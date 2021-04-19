---
description: Das Tool MF Trace kann eine XML-Konfigurationsdatei lesen, die einen oder mehrere Ablauf Verfolgungs Anbieter angibt.
ms.assetid: 70d11a55-041e-4eb5-96a9-238e7ecdd906
title: MF-Ablauf Verfolgungs Konfigurationsdatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6598bcfdde16291fb744783b2f12be414ae997b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355630"
---
# <a name="mftrace-configuration-file"></a>MF-Ablauf Verfolgungs Konfigurationsdatei

Das Tool [MF Trace](mftrace.md) kann eine XML-Konfigurationsdatei lesen, die einen oder mehrere Ablauf Verfolgungs Anbieter angibt.

Das [**Providers**](providers.md) -Element ist das Stamm Element in der Konfigurationsdatei.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [**Schlüsselwort**](keyword.md)
-   [**MF-Umleitungen**](mfdetours.md)
-   [**ab**](provider.md)
-   [**providers**](providers.md)

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

[MF-Ablauf Verfolgung](mftrace.md)
</dt> </dl>

 

 



