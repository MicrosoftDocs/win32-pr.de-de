---
title: Iconfigasfwriter-Methode "Konfigurations Methode"
description: Mit der Methode "konfigurierte Methode" wird der Filter konfiguriert, um eine auf dem angegebenen vordefinierten Profil basierende ASF-Datei zu schreiben. (Veraltet.).
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- Konfigurierten Windows Media-Format für die Methode "Konfigurations Methode"
- Methode "config refilterusingprofileguid" Windows Media-Format, iconfigasfwriter-Schnittstelle
- Iconfigasfwriter-Schnittstelle Windows Media-Format, Methode "config refilterusingprofileguid"
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1521738af4411baa2c11f3d20722e09e2d22a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517024"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a>Iconfigasfwriter:: konfigurifirefilterusingprofileguid-Methode

Mit der Methode " **konfigurierte** Methode" wird der Filter konfiguriert, um eine auf dem angegebenen vordefinierten Profil basierende ASF-Datei zu schreiben. (Veraltet.)

## <a name="syntax"></a>Syntax


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*guidprofile* \[ in\]
</dt> <dd>

**GUID** , die ein Profil identifiziert, das in der Windows Media-Format-SDK-Header Datei "wmsysprf. h" definiert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück.



| Rückgabecode                                                                                         | Beschreibung                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Die Methode wurde erfolgreich ausgeführt.<br/>        |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>              | Das Profil ist ungültig.<br/>    |
| <dl> <dt>**VFW \_ E \_ falscher \_ Zustand**</dt> </dl> | Das Filter Diagramm wurde beendet.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ab dem Windows Media Format 9-Reihe-SDK wurden keine neuen Systemprofile definiert. Mit dieser Methode können nur Systemprofil-GUIDs der Version 8 (oder früher) verwendet werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iconfigasfwriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

