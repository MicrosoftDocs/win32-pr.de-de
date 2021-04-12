---
description: Beschreibt die Dokument Konventionen zum Lesen von WMI-Skript-API-Themen.
ms.assetid: 889e6322-96f6-4a24-a084-e3b7bfa94a40
ms.tgt_platform: multiple
title: Dokument Konventionen für die Skript-API
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33335982672472fa9924a6e250305a3630628b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346739"
---
# <a name="document-conventions-for-the-scripting-api"></a>Dokument Konventionen für die Skript-API

Die [Skript-API für die WMI](scripting-api-for-wmi.md) -Referenz verwendet die folgenden Dokument Konventionen:

-   Parameter Typen werden mit einem Präfix definiert: b (Boolean), Str (String), I (Integer), obj (Automation-Objekt), var (Variant).
-   Optionale Parameter werden in eckigen Klammern mit ihren Standardwerten platziert, die durch die Zuweisung angezeigt werden.
-   Im Fall von Objekt Parametern geben die Zeichen nach dem Präfix "obj" den Objekttyp an, der erwartet wird.



| Object-Parameter      | Objekttyp                                          |
|-----------------------|------------------------------------------------------|
| *Wbemdatetime*        | [**Swap-DateTime**](swbemdatetime.md)               |
| *Wbemeventsource*     | [**"Errbemeventsource"**](swbemeventsource.md)         |
| *Wbemlocator*         | [**SWbemLocator**](swbemlocator.md)                 |
| *Wbemmethod*          | [**Swap-Methode**](swbemmethod.md)                   |
| *Wbemmethodset*       | [**Swap-methodset**](swbemmethodset.md)             |
| *Wbemnamedvalueset*   | [**Austausch Elementname**](swbemnamedvalueset.md)     |
| *Wbemubjekt*          | [**Austausch Objekt**](swbemobject.md)                   |
| *Wbemubjectex*        | [**Austauschen von "errbemubjectex"**](swbemobjectex.md)               |
| *Wbemubjectpath*      | [**Errbemubjectpath**](swbemobjectpath.md)           |
| *Wbemubjectset*       | [**Austauschen von "errbemubjectset"**](swbemobjectset.md)             |
| *Wbemprivilege*       | [**Austausch Berechtigung**](swbemprivilege.md)             |
| *Wbemprivilegeset*    | [**Swap-Privileg**](swbemprivilegeset.md)       |
| *Wbemproperty*        | [**Swap Property**](swbemproperty.md)               |
| *Wbempropertyset*     | [**Swap PropertySet**](swbempropertyset.md)         |
| *Wbemqualifizierer*       | [**Austausch Qualifizierer**](swbemqualifier.md)             |
| *Wbemqualifierset*    | [**Swap-qualifierset**](swbemqualifierset.md)       |
| *Wbemerfrischendes ableitem* | [**Swap-aktuableitem**](swbemrefreshableitem.md) |
| *Wbemfreshsher*       | [**Swap-Aktualisierungs Programm**](swbemrefresher.md)             |
| *WbemServices*        | [**SWbemServices**](swbemservices.md)               |
| *Wbemservicesex*      | [**Swap Service Ex**](swbemservicesex.md)           |



 

Der folgende Code zeigt z. b., wie Sie Variablen für verschiedene Objekttypen benennen:


```VB
strComputerName  ' a string value for a computer name
bStatusFlag  ' a boolean value used for a status
objServices  ' an object value used to store an SWbemServices value
```



 

 



