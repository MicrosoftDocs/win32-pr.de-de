---
description: Proxy Funktion für die GetLocation-Methode.
ms.assetid: 2dc4767b-9992-4e5a-a171-2de19178d912
title: IWICMetadataQueryReader_GetLocation_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetLocation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 40dd23df0e1004687a945889d2598d41ca0e2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351577"
---
# <a name="iwicmetadataqueryreader_getlocation_proxy-function"></a>IWICMetadataQueryReader \_ getLocation- \_ Proxy Funktion

Proxy Funktion für die [**getLocation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICMetadataQueryReader_GetLocation_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    UINT                    cchMaxLength,
  _Inout_ WCHAR                   *wzNamespace,
  _Out_   UINT                    *pcchActualLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _

Zeiger auf dieses [_ *IWICMetadataQueryReader* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) -Objekt.

</dd> <dt>

*cchmaxlength* \[ in\]
</dt> <dd>

Typ: **uint**

Die Länge des *wznamespace* -Puffers.

</dd> <dt>

*wznamespace* \[ in, out\]
</dt> <dd>

Typ: **WCHAR \** _

Ein Zeiger, der den aktuellen Namespace Speicherort empfängt.

</dd> <dt>

_pcchActualLength * \[ out\]
</dt> <dd>

Typ: **uint \** _

Die tatsächliche Pufferlänge, die benötigt wird, um den aktuellen Namespace Speicherort abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




