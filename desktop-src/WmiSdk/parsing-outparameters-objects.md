---
description: Ein SWbemMethod.OutParameters-Objekt wird von der ausgeführten Anbietermethode erstellt und mit Daten bereitgestellt.
ms.assetid: fc06d6a1-770a-4f34-affd-f5035dad9360
ms.tgt_platform: multiple
title: Analysieren von OutParameters-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69c13e7d4d6b74f1c404c77e1ae0cc26d62ad698684ca1c864ebf31871dc62e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117923248"
---
# <a name="parsing-outparameters-objects"></a>Analysieren von OutParameters-Objekten

Ein [**SWbemMethod.OutParameters-Objekt**](swbemmethod-outparameters.md) wird von der ausgeführten Anbietermethode erstellt und mit Daten bereitgestellt. Eigenschaften des **OutParameters-Objekts** sind spezifisch für die aufgerufene Methode. Im folgenden Skript ist *SD* (in *outParam* enthalten) beispielsweise der Ausgabeparameter, der für die **\_ \_ SystemSecurity.GetSD-Methode** definiert ist. Die **ReturnValue-Eigenschaft** ist eine generische Eigenschaft, die für alle **OutParameters-Objekte** verfügbar ist, die das Ergebnis des Vorgangs enthalten.

Das folgende Codebeispiel veranschaulicht das Abrufen von Ausgabeparametern aus der Ausführung der [**GetSD-Methode**](--systemsecurity-getsd.md) in der [**\_ \_ SystemSecurity-Klasse**](--systemsecurity.md) für das lokale System.


```VB
' Connect to WMI root\cimv2 namespace.
Set svc = GetObject("winmgmts:root/cimv2")
' Execute the GetSD method and obtain the output parameters.
set outParam = svc.Execmethod("__SystemSecurity=@", "GetSD")
wscript.echo outparam.ReturnValue
' Format the security descriptor array
' in the SD parameter into one string to display.
objSD  = Join(outparam.SD,",")
wscript.echo objSD
' Release the out parameters object.
set outParam = nothing
```



Weitere Informationen finden Sie unter [**SWbemMethod.InParameters**](swbemmethod-inparameters.md).

 

 



