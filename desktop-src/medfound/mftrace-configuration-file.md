---
description: Das MFTrace-Tool kann eine XML-Konfigurationsdatei lesen, die einen oder mehrere Ablaufverfolgungsanbieter angibt.
ms.assetid: 70d11a55-041e-4eb5-96a9-238e7ecdd906
title: MFTrace-Konfigurationsdatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60969d52405b5aeeb768710d35751d9ea2cab40ca60a7d85a4da1bc1b0c65468
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871937"
---
# <a name="mftrace-configuration-file"></a>MFTrace-Konfigurationsdatei

Das [MFTrace-Tool](mftrace.md) kann eine XML-Konfigurationsdatei lesen, die einen oder mehrere Ablaufverfolgungsanbieter angibt.

Das [**providers-Element**](providers.md) ist das Stammelement in der Konfigurationsdatei.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [**Schlüsselwort**](keyword.md)
-   [**mfdetours**](mfdetours.md)
-   [**Anbieter**](provider.md)
-   [**Anbieter**](providers.md)

## <a name="example"></a>Beispiel

``` syntax
<?xml version='1.0' encoding='utf-8'?>
<providers>
  <mfdetours level="info"> 
    <keyword ID="MFPlatExport" />
  </mfdetours>
  
  <!-- Manifest-based traces -->

  <provider level="verbose" ID="Microsoft-Windows-MediaFoundation-MFReadWrite">
    <keyword ID="0x0000000000000000" />
  </provider>

</providers>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mftrace](mftrace.md)
</dt> </dl>

 

 



