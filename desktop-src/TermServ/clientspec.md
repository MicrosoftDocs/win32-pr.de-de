---
title: Clientspec-Enumeration
description: Wird mit der clientprotocolspec-Eigenschaft zum Angeben des Remote Desktop Protokolls verwendet, das zwischen dem Client und dem Server verwendet wird.
ms.assetid: BFB2CD3C-04BF-4CB3-B156-8B08AE697327
ms.tgt_platform: multiple
keywords:
- Clientspec-Enumeration Remotedesktopdienste
topic_type:
- apiref
api_name:
- ClientSpec
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f52fbdbaa37c392de727dd2640580800d813d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337296"
---
# <a name="clientspec-enumeration"></a>Clientspec-Enumeration

Wird mit der [**clientprotocolspec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) -Eigenschaft zum Angeben des Remote Desktop Protokolls verwendet, das zwischen dem Client und dem Server verwendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  FullMode        = 0,
  ThinClientMode,
  SmallCacheMode
} ClientSpec;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**Fullmode**
</dt> <dd>

Das Protokoll ist vollständiges Windows 8-Remotedesktop Protokoll.

</dd> <dt>

<span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**Thinclientmode**
</dt> <dd>

Das Protokoll ist auf die Verwendung von Windows 7 mit SP1 remotefx-Codec und einem kleineren Cache beschränkt. Alle anderen Codecs sind deaktiviert. Dieses Protokoll verfügt über den kleinsten Speicherbedarf.

</dd> <dt>

<span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**Smallcachemode**
</dt> <dd>

Das Protokoll ist mit dem **fullmode** identisch, mit dem Unterschied, dass es einen kleineren Cache verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings8:: clientprotocolspec**](imsrdpclientadvancedsettings8-clientprotocolspec.md)
</dt> </dl>

 

 





