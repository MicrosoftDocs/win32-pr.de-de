---
description: Erstellt einen Enumerator für die Übertragungsformate, die vom wia 2.0-Gerät (Windows Image Acquisition) unterstützt werden.
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: IWiaTransfer::EnumWIA_FORMAT_INFO-Methode (Wia.h)
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
ms.openlocfilehash: 5e497d389646249c03bfaa4ac8625ce2a440b97f4ff6b8c0b0942ec957d0901e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669475"
---
# <a name="iwiatransferenumwia_format_info-method"></a>IWiaTransfer::EnumWIA \_ FORMAT \_ INFO-Methode

Erstellt einen Enumerator für die Übertragungsformate, die vom wia 2.0-Gerät (Windows Image Acquisition) unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppIEnum* \[ out\]
</dt> <dd>

Typ: **[ **IEnumWIA \_ FORMAT \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***

Die Adresse des Zeigers auf die [**IEnumWIA \_ FORMAT \_ INFO-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) für den Enumerator.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Anwendungen müssen die [IUnknown::Release-Methode](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für den Schnittstellenzeiger aufrufen, der über den *ppIEnum-Parameter* empfangen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
