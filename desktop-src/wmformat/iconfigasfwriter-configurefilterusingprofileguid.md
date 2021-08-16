---
title: IConfigAsfWriter ConfigureFilterUsingProfileGuid-Methode
description: Die ConfigureFilterUsingProfileGuid-Methode konfiguriert den Filter, um eine ASF-Datei basierend auf dem angegebenen vordefinierten Profil zu schreiben. (Veraltet.)
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- ConfigureFilterUsingProfileGuid-Methode windows Media Format
- ConfigureFilterUsingProfileGuid-Methode windows Media Format , IConfigAsfWriter-Schnittstelle
- IConfigAsfWriter-Schnittstelle windows Media Format , ConfigureFilterUsingProfileGuid-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f427dc67695ebaca3e3e7502f2f1961b738a8f775ace394948ef445f3ad9a64e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118703086"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a>IConfigAsfWriter::ConfigureFilterUsingProfileGuid-Methode

Die **ConfigureFilterUsingProfileGuid-Methode** konfiguriert den Filter, um eine ASF-Datei basierend auf dem angegebenen vordefinierten Profil zu schreiben. (Veraltet.)

## <a name="syntax"></a>Syntax


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*guidProfile* \[ In\]
</dt> <dd>

**GUID,** die ein Profil gemäß definition in der Windows Media Format SDK-Headerdatei Wmsysprf.h identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück.



| Rückgabecode                                                                                         | Beschreibung                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Die Methode wurde erfolgreich ausgeführt.<br/>        |
| <dl> <dt>**E \_ FAIL**</dt> </dl>              | Das Profil ist ungültig.<br/>    |
| <dl> <dt>**VFW \_ E \_ WRONG \_ STATE**</dt> </dl> | Das Filterdiagramm wird beendet.<br/> |



 

## <a name="remarks"></a>Hinweise

Ab dem Windows Media Format 9 Series SDK wurden keine neuen Systemprofile definiert. Mit dieser Methode können nur Systemprofil-GUIDs der Version 8 (oder früher) verwendet werden.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IConfigAsfWriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

