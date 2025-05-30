## API Report File for "@backstage-community/plugin-github-deployments"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { BackstagePlugin } from '@backstage/core-plugin-api';
import { Entity } from '@backstage/catalog-model';
import { JSX as JSX_2 } from 'react/jsx-runtime';
import { TableColumn } from '@backstage/core-components';

// @public (undocumented)
export const EntityGithubDeploymentsCard: (props: {
  environments?: string[] | undefined;
  last?: number | undefined;
  lastStatuses?: number | undefined;
  columns?: TableColumn<GithubDeployment>[] | undefined;
}) => JSX_2.Element;

// @public (undocumented)
export const GITHUB_PROJECT_SLUG_ANNOTATION = 'github.com/project-slug';

// @public (undocumented)
export type GithubDeployment = {
  environment: string;
  state: string;
  updatedAt: string;
  commit: {
    abbreviatedOid: string;
    commitUrl: string;
  } | null;
  statuses: {
    nodes: Node_2[];
  };
  creator: {
    login: string;
  };
  repository: {
    nameWithOwner: string;
  };
  payload: string;
};

// @public (undocumented)
export const githubDeploymentsPlugin: BackstagePlugin<{}, {}, {}>;

// @public (undocumented)
export const GithubDeploymentsTable: {
  (props: {
    deployments: GithubDeployment[];
    isLoading: boolean;
    reload: () => void;
    columns: TableColumn<GithubDeployment>[];
  }): JSX_2.Element;
  columns: Readonly<{
    createEnvironmentColumn(): TableColumn<GithubDeployment>;
    createStatusColumn(): TableColumn<GithubDeployment>;
    createCommitColumn(): TableColumn<GithubDeployment>;
    createCreatorColumn(): TableColumn<GithubDeployment>;
    createLastUpdatedColumn(): TableColumn<GithubDeployment>;
  }>;
  defaultDeploymentColumns: TableColumn<GithubDeployment>[];
};

// @public (undocumented)
export const isGithubDeploymentsAvailable: (entity: Entity) => boolean;

// @public (undocumented)
type Node_2 = {
  logUrl?: string;
};
export { Node_2 as Node };
```
