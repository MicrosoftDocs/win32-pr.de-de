---
title: Iconfigasfwriter getcurrentprofileid-Methode
description: Die getcurrentprofileid-Methode ruft die aktuelle Profil-ID ab. (Nur für Windows Media-Format 4,0-Profile.).
ms.assetid: a5162bb1-5fcb-449e-b8d3-624b863e656d
keywords:
- Getcurrentprofileid-Methode Windows Media-Format
- Getcurrentprofileid-Methode Windows Media-Format, iconfigasfwriter-Schnittstelle
- Iconfigasfwriter-Schnittstelle Windows Media-Format, getcurrentprofileid-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416ac2c48f6ec8836a7390f18f38eca3dca35274
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337230"
---
# <a name="iconfigasfwritergetcurrentprofileid-method"></a>Iconfigasfwriter:: getcurrentprofileid-Methode

Die **getcurrentprofileid** -Methode ruft die aktuelle Profil-ID ab. (Nur für Windows Media-Format 4,0-Profile.)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCurrentProfileId(
  [out] DWORD *pdwProfileId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdwprofileid* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable vom Typ **DWORD** , die die aktuelle Profil-ID empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode ist mittlerweile veraltet, da Sie Windows Media-Format-SDK-Profile von Version 4,0 annimmt. Verwenden Sie stattdessen [**iconfigasfwriter:: getcurrentprofile**](iconfigasfwriter-getcurrentprofile.md) oder [**iconfigasfwriter:: getcurrentprofileguid**](iconfigasfwriter-getcurrentprofileguid.md) , um ein Profil für Version 7,0 und höher ordnungsgemäß zu identifizieren.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iconfigasfwriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 