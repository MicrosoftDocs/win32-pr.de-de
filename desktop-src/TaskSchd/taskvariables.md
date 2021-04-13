---
title: TaskVariables-Objekt
description: Skript Objekt, das Task Variablen definiert, die als Parameter an Task Handler und externe ausführbare Dateien, die von Aufgaben gestartet werden, übermittelt werden können.
ms.assetid: 194babe0-16bd-4a78-af45-139c9c7eacbe
keywords:
- TaskVariables-Objekt Taskplaner
- TaskVariables-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- TaskVariables
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fe20153b0d6d66ca6c7f263a8e76d5a4d480b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478351"
---
# <a name="taskvariables-object"></a>TaskVariables-Objekt

Skript Objekt, das Task Variablen definiert, die als Parameter an Task Handler und externe ausführbare Dateien, die von Aufgaben gestartet werden, übermittelt werden können.

## <a name="members"></a>Member

Das **taskVariables** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **taskVariables** -Objekt verfügt über diese Methoden.



| Methode                                         | BESCHREIBUNG                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**GetContext**](taskvariables-getcontext.md) | Wird verwendet, um den Kontext zwischen verschiedenen Schritten und Aufgaben zu teilen, die sich in derselben Auftrags Instanz befinden.<br/> |
| [**GetInput**](taskvariables-getinput.md)     | Ruft die Eingabevariablen für eine Aufgabe ab.<br/>                                                           |
| [**SetOutput**](taskvariables-setoutput.md)   | Legt die Ausgabevariablen für eine Aufgabe fest.<br/>                                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





