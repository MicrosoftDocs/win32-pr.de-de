---
description: Die viewbillboard-Methode des uipreview-Objekts zeigt ein erstelltes Billboard mithilfe des Host Steuer Elements im momentan angezeigten Dialogfeld an.
ms.assetid: c51c1a5b-af53-47a8-9281-e790efadcfc4
title: Uipreview. viewbillboard-Methode
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
ms.openlocfilehash: 9cf1c6ee2a47fdb246fcc847627bb63432b8a67f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356473"
---
# <a name="uipreviewviewbillboard-method"></a>Uipreview. viewbillboard-Methode

Die **viewbillboard** -Methode des [**uipreview**](uipreview-object.md) -Objekts zeigt ein erstelltes Billboard mithilfe des Host Steuer Elements im momentan angezeigten Dialogfeld an.

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

Der erforderliche Name des-Steuer Elements, das das Billboard (Unterscheidung nach Groß-/Kleinschreibung) mit dem Dialogfeld und die Primärschlüssel der Steuerungsdaten Bank Tabelle gehostet.

</dd> <dt>

*Billboard* 
</dt> <dd>

Der erforderliche Name des mit dem angegebenen Steuerelement und dem aktuellen Dialogfeld anzuzeigenden Billboards und der Primärschlüssel der Tabelle mit den Datenbanktabellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iuipreview ist definiert als 000c109a-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




