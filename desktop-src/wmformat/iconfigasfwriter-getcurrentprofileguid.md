---
title: IConfigAsfWriter GetCurrentProfileGuid-Methode
description: Die GetCurrentProfileGuid-Methode ruft die aktuelle Windows Profil-GUID des Mediensystems ab.
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- 'GetCurrentProfileGuid-Methode : Windows Media Format'
- GetCurrentProfileGuid-Methode windows Media Format , IConfigAsfWriter-Schnittstelle
- IConfigAsfWriter-Schnittstelle windows Media Format , GetCurrentProfileGuid-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ae1c626658509d4260f814550c053de7389b0aed45c9c583e0e059e390a24f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433639"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a>IConfigAsfWriter::GetCurrentProfileGuid-Methode

Die **GetCurrentProfileGuid-Methode** ruft die aktuelle Windows Profil-GUID des Mediensystems ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pProfileGuid* \[ out\]
</dt> <dd>

Zeiger auf eine Variable vom Typ **GUID,** die das aktuelle Systemprofil identifiziert, das vom Filter verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Wenn ein Fehler auftritt, wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode wird nicht mit benutzerdefinierten Profilen verwendet (einschließlich aller Profile, die Streams enthalten, die die Windows Media Audio- und Videocodecs verwenden), da alle diese Profile von Anwendungen erstellt werden und keinen GUID-Bezeichner haben. Wenn kein Systemprofil geladen wird, *wird pProfileGuid* auf **NULL festgelegt.**

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IConfigAsfWriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 