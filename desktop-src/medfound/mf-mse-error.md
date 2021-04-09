---
description: Definiert die verschiedenen Fehlerzustände der Medienquellen Erweiterung.
ms.assetid: 8FD54833-F60B-49E8-A673-6130F3B06160
title: MF_MSE_ERROR-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_ERROR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 6b6aaea772376b0e57c006a56a5a1bb30bc497c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130717"
---
# <a name="mf_mse_error-enumeration"></a>MF- \_ MSE- \_ Fehler Enumeration

Definiert die verschiedenen Fehlerzustände der Medienquellen Erweiterung.

## <a name="syntax"></a>Syntax


```C++
typedef enum _MF_MSE_ERROR { 
  MF_MSE_ERROR_NOERROR        =  0,
  MF_MSE_ERROR_NETWORK        = 1,
  MF_MSE_ERROR_DECODE         = 2,
  MF_MSE_ERROR_UNKNOWN_ERROR  =  3
} MF_MSE_ERROR;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**MF- \_ MSE- \_ Fehler \_ noError**
</dt> <dd>

Gibt keinen Fehler an.

</dd> <dt>

<span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**Netzwerk für MF- \_ MSE- \_ Fehler \_**
</dt> <dd>

Gibt einen Fehler im Netzwerk an.

</dd> <dt>

<span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**\_ \_ Fehler beim \_ Decodieren von MF-MSE**
</dt> <dd>

Gibt einen Fehler beim Decodieren an.

</dd> <dt>

<span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**Unbekannter Fehler im MF-MSE-Fehler. \_ \_ \_ \_**
</dt> <dd>

Gibt einen unbekannten Fehler an.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>MF mediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Enumerationen](media-foundation-enumerations.md)
</dt> </dl>

 

 




