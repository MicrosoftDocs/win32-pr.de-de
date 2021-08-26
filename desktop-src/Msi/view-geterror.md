---
description: Die GetError-Methode des View-Objekts gibt den Validierungsfehler und den Spaltennamen zurück, für den der Fehler aufgetreten ist.
ms.assetid: ca90dfa5-8e15-490c-835b-c5c225c3cc7b
title: View.GetError-Methode
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
ms.openlocfilehash: ddbed26565598ad58b3605b7c70a9a5bbede3e5282ff4a7fa011df5c56bd8b31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038800"
---
# <a name="viewgeterror-method"></a>View.GetError-Methode

Die **GetError-Methode** des [**View-Objekts**](view-object.md) gibt den Validierungsfehler und den Spaltennamen zurück, für den der Fehler aufgetreten ist. In der Automatisierung ist der zurückgegebene Wert eine Zeichenfolge im Format \# \# ColumnName, wobei die \# \# einen zweistelligen Fehlercode darstellt. Sie gibt den ersten Fehler im Fehlerarray der Ansicht zurück. Nachfolgende Aufrufe geben den nächsten Wert im Fehlerarray zurück. Sobald der Wert "00" zurückgegeben wurde, sind keine weiteren Fehler mehr vorhanden, und nachfolgende Aufrufe durchlaufen das Array einfach erneut.

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
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView ist als 000C109C-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                                |



 

 




