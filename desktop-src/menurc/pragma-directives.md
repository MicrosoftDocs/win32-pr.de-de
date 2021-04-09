---
title: Pragma-Direktiven
description: RC unterstützt die vom C/C++-Compiler unterstützten pragma-Direktiven nicht.
ms.assetid: c7a944c0-a3d4-4568-a9ac-c338f0eaa427
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab0c92136ba5e00d5b821d35ea05a337e7d6abe7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038967"
---
# <a name="pragma-directives"></a>Pragma-Direktiven

RC unterstützt die vom C/C++-Compiler unterstützten pragma-Direktiven nicht. RC unterstützt jedoch die folgende pragma-Direktive zum Ändern der Codepage:

``` syntax
#pragma code_page( [ DEFAULT | CodePageNum ] )
```

Dieses Pragma wird in einer enthaltenen Ressourcen Datei (. RC) nicht unterstützt. Wenn Sie also über eine übergeordnete RC-Datei verfügen und RC-Dateien für mehrere Sprachen enthalten, verwenden Sie dieses Pragma vor dem Einschließen einer anderen RC-Datei, anstatt Sie in der enthaltenen RC-Datei selbst zu verwenden. Dies wird im folgenden Beispiel veranschaulicht.

``` syntax
#include "English.rc"
#pragma code_page(932)
#include "Japanese.rc"
```

Eine Liste der Werte für codepagenum finden Sie unter [Code Page Identifier](../intl/code-page-identifiers.md).

 

 