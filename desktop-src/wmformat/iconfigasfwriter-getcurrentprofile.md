---
title: IConfigAsfWriter GetCurrentProfile-Methode
description: Die GetCurrentProfile-Methode ruft das anwendungsdefinierte Profil ab.
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- GetCurrentProfile-Methode windows Media Format
- GetCurrentProfile-Methode windows Media Format , IConfigAsfWriter-Schnittstelle
- IConfigAsfWriter-Schnittstelle windows Media Format , GetCurrentProfile-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b7a07ed6ab5b94138c0c04d40782496535e0ae4a3eff0f443c89d7ccd0c4b1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118198381"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a>IConfigAsfWriter::GetCurrentProfile-Methode

Die **GetCurrentProfile-Methode** ruft das anwendungsdefinierte Profil ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppProfile* \[ out\]
</dt> <dd>

Adresse eines Zeigers, der die [**IWMProfile-Schnittstelle**](iwmprofile.md) des anwendungsdefinierte Profils empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Wenn ein Fehler auftritt, wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn die Methode erfolgreich ist, weist der **zurückgegebene IWMProfile-Zeiger** einen ausstehenden Verweiszähler auf. Stellen Sie sicher, dass Sie die Schnittstelle freigeben, wenn Sie sie nicht mehr verwenden.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IConfigAsfWriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 