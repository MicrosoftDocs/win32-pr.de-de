---
title: Iconfigasfwriter getcurrentprofile-Methode
description: Die getcurrentprofile-Methode ruft das Anwendungs definierte Profil ab.
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- Getcurrentprofile-Methode Windows Media-Format
- Getcurrentprofile-Methode Windows Media-Format, iconfigasfwriter-Schnittstelle
- Iconfigasfwriter-Schnittstelle Windows Media-Format, getcurrentprofile-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88931d83674ffa84288b4bec10e3c9dba15c812a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338069"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a>Iconfigasfwriter:: getcurrentprofile-Methode

Die **getcurrentprofile** -Methode ruft das Anwendungs definierte Profil ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppprofile* \[ vorgenommen\]
</dt> <dd>

Adresse eines Zeigers, der die [**iwmprofile**](iwmprofile.md) -Schnittstelle des Anwendungs definierten Profils empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn die Methode erfolgreich ausgeführt wird, weist der zurückgegebene **iwmprofile** -Zeiger einen ausstehenden Verweis Zähler auf. Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iconfigasfwriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 