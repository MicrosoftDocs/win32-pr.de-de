---
description: Die ViewDialog-Methode des UIPreview-Objekts zeigt ein in der aktuellen Datenbank gespeichertes Dialogfeld für die benutzeroberfläche an.
ms.assetid: 5bc935ac-38ca-4a51-a1dc-6879dee97b05
title: UIPreview.ViewDialog-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewDialog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 40797da833576c0a829234d6036cb1d583464dea96dbe4e625dcd63c1c1bd4c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893400"
---
# <a name="uipreviewviewdialog-method"></a>UIPreview.ViewDialog-Methode

Die **ViewDialog-Methode** des [**UIPreview-Objekts**](uipreview-object.md) zeigt ein in der aktuellen Datenbank gespeichertes Dialogfeld für die benutzeroberfläche an.

## <a name="syntax"></a>Syntax


```JScript
UIPreview.ViewDialog(
  dialog
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dialog* 
</dt> <dd>

Erforderlicher Name des Dialogfelds, bei dem die Schreibung beachtet wird, und der Primärschlüssel der Dialogdatenbanktabelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview ist als 000C109A-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



 

 




