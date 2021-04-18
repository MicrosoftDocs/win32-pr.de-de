---
description: Die GetError-Methode des View-Objekts gibt den Überprüfungs Fehler und den Spaltennamen zurück, für den der Fehler aufgetreten ist.
ms.assetid: ca90dfa5-8e15-490c-835b-c5c225c3cc7b
title: View. GetError-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.GetError
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1305bf6f497e92ff4d455a696179a943df8a057b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366002"
---
# <a name="viewgeterror-method"></a>View. GetError-Methode

Die **getError** -Methode des [**View**](view-object.md) -Objekts gibt den Überprüfungs Fehler und den Spaltennamen zurück, für den der Fehler aufgetreten ist. In Automation ist der zurückgegebene Wert eine Zeichenfolge der Form \# \# ColumnName, wobei der \# \# einen zweistelligen Fehlercode darstellt. Gibt den ersten Fehler im Fehler Array der Ansicht zurück. nachfolgende Aufrufe geben den nächsten Wert im Fehler Array zurück. Sobald der Wert "00" zurückgegeben wird, sind keine weiteren Fehler mehr vorhanden, und nachfolgende Aufrufe durchlaufen das Array lediglich erneut.

## <a name="syntax"></a>Syntax


```JScript
View.GetError()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView ist definiert als 000c109c-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




