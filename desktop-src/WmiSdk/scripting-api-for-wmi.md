---
description: Die WMI-Skript Referenz enthält Definitionen für die WMI-Skript-API.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: Skript-API für WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c43587fd8f40c2524bcabd79fe80e3d00d74b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863799"
---
# <a name="scripting-api-for-wmi"></a>Skript-API für WMI

Die WMI-Skript Referenz enthält Definitionen für die WMI-Skript-API. Verwenden Sie diese API, wenn Sie Anwendungen mit Microsoft Visual Basic, Visual Basic for Applications, Visual Basic Scripting Edition (VBScript) oder einer beliebigen anderen Skriptsprache schreiben, die Active Scripting-Technologien unterstützt.

> [!Note]  
> PowerShell ist auch für die Skripterstellung mit WMI verfügbar. Das Cmdlet "Get-WMI" und die drei typbeschleuniger ( \[ WMI \] , \[ WMIClass \] und \[ wmisearcher \] ) ermöglichen den grundlegenden administrativen Zugriff auf WMI. Weitere Informationen finden Sie unter [Skripterstellung mit Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).

 

WMI-Skript Objekte, mit Ausnahme von " [**Swap DateTime**](swbemdatetime.md) ", sind nicht als sichere Skripts für Skripts gekennzeichnet, die auf HTML-Seiten in Internet Explorer ausgeführt werden. Wenn die Sicherheitsstufe in Internet Explorer nicht gesenkt wird, schlägt das Skript fehl. " **Taubemdatetime** " ist für die Initialisierung und Skripterstellung als sicher markiert. Verwenden Sie allerdings alle WMI-Skript Objekte in **GetObject** -und **kreateobject** -aufrufen auf Server seitigem Code in Active Server Pages (ASP).

-   [Skript-API-Objektmodell](scripting-api-object-model.md)
-   [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md)
-   [API-Skript Objekte](scripting-api-objects.md)
-   [Skript-API-Konstanten](scripting-api-constants.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Referenz](wmi-reference.md)
</dt> <dt>

[WMI-Rückgabe Codes](wmi-return-codes.md)
</dt> </dl>

 

 



