---
title: Iconfigasfwriter-Methode "konfigurifisingprofileid"
description: Die Methode "konfigurierte Methode" konfiguriert den Filter zum Schreiben einer ASF-Datei mit einem Profil Bezeichner (ID)-Index aus der Liste "Systemprofile". (Nur für Windows Media-Format 4,0-Profile.).
ms.assetid: b0375785-83db-4540-aca9-7ba0bb81c1ef
keywords:
- Konfigurierungs Methode für das Windows Media-Format
- Konfigurations-/filterusingprofileid-Methode Windows Media-Format, iconfigasfwriter-Schnittstelle
- Iconfigasfwriter-Schnittstelle Windows Media-Format, Configuration Report User User-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0226195d7657667e3947b55546b321edafa7befc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340276"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileid-method"></a>Iconfigasfwriter:: konfiguriert refilterusingprofileid-Methode

Die Methode " **konfigurierte** Methode" konfiguriert den Filter zum Schreiben einer ASF-Datei mit einem Profil Bezeichner (ID)-Index aus der Liste "Systemprofile". (Nur für Windows Media-Format 4,0-Profile.)

## <a name="syntax"></a>Syntax


```C++
HRESULT ConfigureFilterUsingProfileId(
  [in] DWORD dwProfileId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwprofileid* \[ in\]
</dt> <dd>

Profil-ID gemäß der Definition in Version 4,0 des Windows Media Format SDK.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück.



| Rückgabecode                                                                                         | Beschreibung                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Die Methode wurde erfolgreich ausgeführt.<br/>        |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>              | Das Profil ist ungültig.<br/>    |
| <dl> <dt>**VFW \_ E \_ falscher \_ Zustand**</dt> </dl> | Das Filter Diagramm wurde beendet.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ist mittlerweile veraltet, da Sie Windows Media-Format-SDK-Profile von Version 4,0 annimmt. Verwenden Sie [**iconfigasfwriter:: Configure refilterusingprofile**](iconfigasfwriter-configurefilterusingprofile.md) oder [**iconfigasfwriter:: Configure refilterusingprofileguid**](iconfigasfwriter-configurefilterusingprofileguid.md), um den Filter für Profile der Version 7,0 und höher zu konfigurieren.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iconfigasfwriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

