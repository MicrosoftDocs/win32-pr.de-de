---
description: Erstellt einen Enumerator für die Übertragungs Formate, die vom Windows-Abbild Erfassungsgerät (WIA) 2,0 unterstützt werden.
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: 'Iwiatransfer:: EnumWIA_FORMAT_INFO-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.EnumWIA_FORMAT_INFO
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 66f3c91d6023655daf85b2a0d726d98a685b001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354497"
---
# <a name="iwiatransferenumwia_format_info-method"></a>Iwiatransfer:: enumwia- \_ Format \_ Info-Methode

Erstellt einen Enumerator für die Übertragungs Formate, die vom Windows-Abbild Erfassungsgerät (WIA) 2,0 unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppiumum* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ienumwia- \_ Format \_ Informationen**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***

Die Adresse des Zeigers auf die [**ienumwia- \_ Format \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) -Schnittstelle für den Enumerator.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für den Schnittstellen Zeiger aufrufen, der über den *ppienum* -Parameter empfangen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
