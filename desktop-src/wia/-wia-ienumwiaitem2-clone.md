---
description: Erstellt eine zusätzliche Instanz der IEnumWiaItem2-Schnittstelle und sendet einen Zeiger darauf zurück.
ms.assetid: 0d36d555-d0d9-4a1c-ac54-de611850449c
title: 'IEnumWiaItem2:: Clone-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Clone
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3279e7db3efe66e940adbcb9677204e5df7867f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752872"
---
# <a name="ienumwiaitem2clone-method"></a>IEnumWiaItem2:: Clone-Methode

Erstellt eine zusätzliche Instanz der [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) -Schnittstelle und sendet einen Zeiger darauf zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [out] IEnumWiaItem2 **ppIEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppiumum* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Empfängt die Adresse der [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) -Schnittstellen Instanz, die von **IEnumWiaItem2:: Clone** erstellt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppienum* -Parameter empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
