---
title: Iconfigasfwriter getcurrentprofileguid-Methode
description: Die getcurrentprofileguid-Methode ruft die aktuelle Windows Media Systemprofile-GUID ab.
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- Getcurrentprofileguid-Methode Windows Media-Format
- Getcurrentprofileguid-Methode Windows Media-Format, iconfigasfwriter-Schnittstelle
- Iconfigasfwriter-Schnittstelle Windows Media-Format, getcurrentprofileguid-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49282ed6ea33db8052e167568e5b5fa70cda9e01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316125"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a>Iconfigasfwriter:: getcurrentprofileguid-Methode

Die **getcurrentprofileguid** -Methode ruft die aktuelle Windows Media Systemprofile-GUID ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pprofileguid* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable vom Typ **GUID** , die das aktuelle Systemprofil identifiziert, das vom Filter verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird nicht mit benutzerdefinierten Profilen verwendet (einschließlich aller Profile, die Streams enthalten, die die Windows Media Audio und Video Codecs verwenden), da alle diese Profile von Anwendungen erstellt werden und keinen GUID-Bezeichner aufweisen. Wenn kein Systemprofil geladen wird, wird *pprofileguid* auf **null** festgelegt.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iconfigasfwriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 