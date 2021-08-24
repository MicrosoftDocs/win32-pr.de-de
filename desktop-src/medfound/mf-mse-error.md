---
description: Definiert die verschiedenen Fehlerzustände der Medienquellenerweiterung.
ms.assetid: 8FD54833-F60B-49E8-A673-6130F3B06160
title: MF_MSE_ERROR Enumeration
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
ms.openlocfilehash: 71246aaa2897540b272360a790718f8d5900934108c98dfcc6b4023898f9f2db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104586"
---
# <a name="mf_mse_error-enumeration"></a>MF \_ MSE \_ ERROR-Enumeration

Definiert die verschiedenen Fehlerzustände der Medienquellenerweiterung.

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

<span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**\_MF-MSE-FEHLER \_ \_ NOERROR**
</dt> <dd>

Gibt keinen Fehler an.

</dd> <dt>

<span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**MF \_ MSE \_ ERROR \_ NETWORK**
</dt> <dd>

Gibt einen Fehler mit dem Netzwerk an.

</dd> <dt>

<span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**\_ \_ MF-MSE-FEHLERDECODIERUNG \_**
</dt> <dd>

Gibt einen Fehler bei der Decodierung an.

</dd> <dt>

<span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**\_MF-MSE-FEHLER \_ \_ UNBEKANNTER \_ FEHLER**
</dt> <dd>

Gibt einen unbekannten Fehler an.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Enumerationen](media-foundation-enumerations.md)
</dt> </dl>

 

 




