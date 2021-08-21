---
description: Die ViewBillboard-Methode des UIPreview-Objekts zeigt mithilfe des Hoststeuerelementes im aktuell angezeigten Dialogfeld einen erstellten Zettel an.
ms.assetid: c51c1a5b-af53-47a8-9281-e790efadcfc4
title: UIPreview.ViewBillboard-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewBillboard
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9892dc68ae5edb66759e4c19499af56d06fb6efac56b823821cd74c4a28644b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810370"
---
# <a name="uipreviewviewbillboard-method"></a>UIPreview.ViewBillboard-Methode

Die **ViewBillboard-Methode** des [**UIPreview-Objekts**](uipreview-object.md) zeigt mithilfe des Hoststeuerelementes im aktuell angezeigten Dialogfeld einen erstellten Zettel an.

## <a name="syntax"></a>Syntax


```JScript
UIPreview.ViewBillboard(
  control,
  billboard
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*control* 
</dt> <dd>

Erforderlicher Name des Steuerelements, das das Steuerelement hosten soll, Groß-/Kleinschreibung wird beachtet, zusammen mit dem Dialogfeld und den Primärschlüsseln der Datenbanktabelle "Control".

</dd> <dt>

*Billboard* 
</dt> <dd>

Erforderlicher Name der Tafel, die mithilfe des angegebenen Steuerelements und des aktuellen Dialogfelds angezeigt werden soll, und der Primärschlüssel der Datenbanktabelle "Nach"

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview ist als 000C109A-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



 

 




