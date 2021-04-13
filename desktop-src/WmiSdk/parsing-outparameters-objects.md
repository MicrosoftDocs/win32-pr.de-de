---
description: Ein-Objekt vom Typ"Swap-Methode. OutParameters" wird erstellt und von der ausgeführten Anbieter Methode mit Daten bereitgestellt.
ms.assetid: fc06d6a1-770a-4f34-affd-f5035dad9360
ms.tgt_platform: multiple
title: Übernehmen von outparameter-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ae3c5d57e9984fceef55de278ed92eba520
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348898"
---
# <a name="parsing-outparameters-objects"></a>Übernehmen von outparameter-Objekten

Ein-Objekt vom Typ" [**Swap-Methode. OutParameters**](swbemmethod-outparameters.md) " wird erstellt und von der ausgeführten Anbieter Methode mit Daten bereitgestellt. Eigenschaften des **OutParameters** -Objekts sind spezifisch für die Methode, die aufgerufen wird. Im folgenden Skript ist *SD* (in *outParam* enthalten) z. b. der Output-Parameter, der für die **\_ \_ System Security. getd-** Methode definiert ist. Die **ReturnValue** -Eigenschaft ist eine generische Eigenschaft, die für alle **OutParameters** -Objekte verfügbar ist, die das Ergebnis des Vorgangs enthalten.

Das folgende Codebeispiel veranschaulicht das Abrufen von Ausgabeparametern aus der Ausführung der [**gezd-**](--systemsecurity-getsd.md) Methode in der Klasse [**\_ \_ SystemSecurity**](--systemsecurity.md) für das lokale System.


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



Weitere Informationen finden Sie unter " [**Swap method. InParameters**](swbemmethod-inparameters.md)".

 

 



