---
title: IConfigAsfWriter GetCurrentProfileId-Methode
description: Die GetCurrentProfileId-Methode ruft die aktuelle Profil-ID ab. (Nur für Windows Media Format 4.0-Profile.)
ms.assetid: a5162bb1-5fcb-449e-b8d3-624b863e656d
keywords:
- GetCurrentProfileId-Methode windows Media Format
- GetCurrentProfileId-Methode windows Media Format, IConfigAsfWriter-Schnittstelle
- IConfigAsfWriter-Schnittstelle windows Media Format , GetCurrentProfileId-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e065e15b0c73b4b1037003dee936af5f74208e4433c6925594e18ab92319028c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655475"
---
# <a name="iconfigasfwritergetcurrentprofileid-method"></a>IConfigAsfWriter::GetCurrentProfileId-Methode

Die **GetCurrentProfileId-Methode** ruft die aktuelle Profil-ID ab. (Nur für Windows Media Format 4.0-Profile.)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCurrentProfileId(
  [out] DWORD *pdwProfileId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdwProfileId* \[ out\]
</dt> <dd>

Zeiger auf eine Variable vom Typ **DWORD,** die die aktuelle Profil-ID empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Wenn ein Fehler auftritt, wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode ist jetzt veraltet, da sie version 4.0 Windows Media Format SDK-Profilen an. Verwenden [**Sie stattdessen IConfigAsfWriter::GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) oder [**IConfigAsfWriter::GetCurrentProfileGuid,**](iconfigasfwriter-getcurrentprofileguid.md) um ein Profil für Version 7.0 und höher ordnungsgemäß zu identifizieren.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IConfigAsfWriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 