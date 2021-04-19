---
description: Die getmaximumcursors-Methode ruft die maximale Anzahl von Cursorn ab, die ein Tablet-Gerät unterstützt.
ms.assetid: 5a43d792-e64c-4506-9792-31efe0885959
title: 'ITablet3:: getmaximumcursors-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.GetMaximumCursors
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7c40184d35ac1d42cb5f5e845396b40efc2d928e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362551"
---
# <a name="itablet3getmaximumcursors-method"></a>ITablet3:: getmaximumcursors-Methode

Die **getmaximumcursors** -Methode ruft die maximale Anzahl von Cursorn ab, die ein Tablet-Gerät unterstützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMaximumCursors(
   ULONG *pMaximumCursors
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmaximumcursors* 
</dt> <dd>

Die maximale Anzahl von Eingaben, die das Gerät unterstützt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK zurück; andernfalls wird ein Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITablet3**](itablet3.md)
</dt> </dl>

 

 




