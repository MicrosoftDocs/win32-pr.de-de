---
description: Die componentcosts-Eigenschaft des Session-Objekts gibt ein RecordList-Objekt zurück, das den für die Installation einer Komponente erforderlichen Speicherplatz pro Laufwerk auflistet.
ms.assetid: 9b1355f1-cc99-49d9-8187-07fba4804d1f
title: Session. componentcosts (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCosts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6ef4e3bfd441f5de61c0f3d69aea93d6cfd2ed8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369689"
---
# <a name="sessioncomponentcosts-property"></a>Session. componentcosts (Eigenschaft)

Die componentcosts-Eigenschaft des [**Session**](session-object.md) -Objekts gibt ein [**RecordList**](recordlist-object.md) -Objekt zurück, das den für die Installation einer Komponente erforderlichen Speicherplatz pro Laufwerk auflistet. Diese Informationen werden von der Benutzeroberfläche verwendet, um den erforderlichen Speicherplatz für alle Laufwerke anzuzeigen. Die zurückgegebenen Speicherplatz Kosten liegen in Vielfachen von 512 Bytes.

Die componentcosts-Eigenschaft sollte nur verwendet werden, nachdem das Installationsprogramm die [Datei Kosten](file-costing.md) und nach der [costfinalize-Aktion](costfinalize-action.md)abgeschlossen hat.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.ComponentCosts
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Um die Gesamtkosten zu erhalten, fügen Sie die Kosten für alle Komponenten zuzüglich der Kosten für den Installer-Engine (Component = "") hinzu.

Componentcosts gibt ein [**RecordList-Objekt**](recordlist-object.md)zurück. Jeder Datensatz im zurückgegebenen RecordList-Objekt verfügt über die folgenden Felder:



| Feld | BESCHREIBUNG                                          |
|-------|------------------------------------------------------|
| 1     | Volume/Laufwerks Name                                    |
| 2     | Der endgültige Speicherplatz Kosten in Vielfachen von 512 Bytes.     |
| 3     | Temporäre Speicherplatz Kosten in Vielfachen von 512 Bytes. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




