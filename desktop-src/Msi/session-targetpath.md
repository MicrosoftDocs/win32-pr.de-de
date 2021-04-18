---
description: Bei der TargetPath-Eigenschaft des Sitzungs Objekts handelt es sich um eine Eigenschaft mit Lese-/Schreibzugriff, die den vollständigen Pfad zum angegebenen Ordner auf dem Installationsziel Laufwerk bereitstellt.
ms.assetid: 563b874e-c669-4f5b-b3fa-eeb6b6e578f2
title: Session. TargetPath (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.TargetPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6c5917f845da0eec944e797d5f49f52d0ec26913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364467"
---
# <a name="sessiontargetpath-property"></a>Session. TargetPath (Eigenschaft)

Bei der **TargetPath** -Eigenschaft des [**Sitzungs**](session-object.md) Objekts handelt es sich um eine Eigenschaft mit Lese-/Schreibzugriff, die den vollständigen Pfad zum angegebenen Ordner auf dem Installationsziel Laufwerk bereitstellt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.TargetPath
Session.TargetPath = propVal 
```



## <a name="property-value"></a>Eigenschaftswert

Unter Berücksichtigung der Groß-/Kleinschreibung für eine Ordner Eigenschaft, die durch einen Primärschlüssel der [Verzeichnis Tabelle](directory-table.md)angegeben wird. Wenn der Ordner nicht vorhanden ist, wird ein Fehler generiert.

## <a name="remarks"></a>Bemerkungen

Versuchen Sie nicht, den Zielpfad zu konfigurieren, wenn die Komponenten, die diese Pfade verwenden, für den aktuellen Benutzer oder für einen anderen Benutzer bereits installiert sind. Überprüfen Sie die Eigenschaft [**productstate**](productstate.md) , um zu bestimmen, ob das Produkt, das die Komponente enthält, installiert ist.

Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




