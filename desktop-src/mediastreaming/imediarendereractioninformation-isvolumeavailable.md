---
title: IMediaRendererActionInformation IsVolumeAvailable-Methode
description: Ruft einen Wert ab, der angibt, ob die DMR die Audiovolumenebene anpassen kann.
ms.assetid: 6DFDC37A-3304-4CDB-9928-C113D2F64ED0
keywords:
- IsVolumeAvailable-Methode Medienstreaming-API
- 'IsVolumeAvailable-Methode: Media Streaming-API, IMediaRendererActionInformation-Schnittstelle'
- IMediaRendererActionInformation-Schnittstelle Media Streaming-API, IsVolumeAvailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsVolumeAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce36a9151998a5f7b0a7785aebc1795bd29d31ff47cfdd2368978ad040f3597c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972209"
---
# <a name="imediarendereractioninformationisvolumeavailable-method"></a>IMediaRendererActionInformation::IsVolumeAvailable-Methode

Ruft einen Wert ab, der angibt, ob die DMR die Audiovolumenebene anpassen kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsVolumeAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Ein boolescher Wert, der **True** ist, wenn die DMR  die Audiovolumenebene anpassen kann, ander denn, false.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

