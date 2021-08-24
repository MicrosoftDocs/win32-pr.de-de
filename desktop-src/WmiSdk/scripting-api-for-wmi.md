---
description: Der WMI-Skriptverweis enthält Definitionen für die WMI-Skripterstellungs-API.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: Skripterstellungs-API für WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35045aa8528c5a3c27475fff753478bd2202d9137cec6b019039aac52775f70a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640540"
---
# <a name="scripting-api-for-wmi"></a>Skripterstellungs-API für WMI

Der WMI-Skriptverweis enthält Definitionen für die WMI-Skripterstellungs-API. Verwenden Sie diese API, wenn Sie Anwendungen mit Microsoft Visual Basic, Visual Basic for Applications, Visual Basic Scripting Edition (VBScript) oder einer anderen Skriptsprache schreiben, die aktive Skripttechnologien unterstützt.

> [!Note]  
> PowerShell ist auch für Skripts mit WMI verfügbar. Das Cmdlet Get-WMI und die drei Typbeschleunigungen \[ (wmi, \] \[ wmiclass \] und \[ wmisearcher) \] ermöglichen den grundlegenden administratorischen Zugriff auf WMI. Weitere Informationen finden Sie unter [Skripterstellung mit Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).

 

WMI-Skriptobjekte mit Ausnahme von [**SWbemDateTime**](swbemdatetime.md) sind für Skripts, die auf HTML-Seiten in Internet Explorer ausgeführt werden, nicht als sicher gekennzeichnet. Daher schlägt das Skript fehl, es sei denn, die Sicherheitsstufe innerhalb Internet Explorer wird gesenkt. **SWbemDateTime** ist für Initialisierung und Skripterstellung als sicher gekennzeichnet. Verwenden Sie jedoch alle WMI-Skriptobjekte in **GetObject-** und **CreateObject-Aufrufen** für serverseitigen Code in Active Server Pages (ASP).

-   [Skripterstellung für API-Objektmodell](scripting-api-object-model.md)
-   [Dokumentkonventionen für die Skripterstellungs-API](document-conventions-for-the-scripting-api.md)
-   [Skripterstellung für API-Objekte](scripting-api-objects.md)
-   [Skripterstellungs-API-Konstanten](scripting-api-constants.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Referenz](wmi-reference.md)
</dt> <dt>

[WMI-Rückgabecodes](wmi-return-codes.md)
</dt> </dl>

 

 



