```ts
import { ReactNode } from "react";

export function TestButton({ icon }: { icon: () => ReactNode }) {
  return <div>{icon()}</div>;
}
```

```ts
import {
  IconAlignLeft,
  IconAlipayCircle,
  IconDelete,
  IconPlus
} from "@arco-design/web-react/icon";
import { TestButton } from "./TestButton";
import { Button } from "@arco-design/web-react";

function Test() {
  return (
    <TestButton
      icon={function () {
        const iconDelete = () => <IconDelete />;
        const iconLeft = () => <IconAlignLeft />;
        return <IconPlus />;
      }}
    />
  );
}

function Haha() {
  return <Button icon={<IconAlipayCircle />} />;
}
```
