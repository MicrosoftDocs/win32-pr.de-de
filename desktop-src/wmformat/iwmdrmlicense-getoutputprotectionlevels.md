---
title: IWMDRMLicense GetOutputProtectionLevels-Methode
description: Die GetOutputProtectionLevels-Methode ruft Informationen zu allen Ausgabeschutzebenen (OUTPUT Protection Levels, OPLs) ab, die der Lizenz zugewiesen sind.
ms.assetid: 6596171a-67ac-42cd-80d9-f77507fc58eb
keywords:
- GetOutputProtectionLevels-Methode windows Media Format
- GetOutputProtectionLevels-Methode windows Media Format, IWMDRMLicense-Schnittstelle
- IWMDRMLicense-Schnittstelle windows Media Format , GetOutputProtectionLevels-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetOutputProtectionLevels
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8d70aaae5e96b8328c091e49836ae743c0fd5ef9d5036fd5aca067f9305d7fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771320"
---
# <a name="iwmdrmlicensegetoutputprotectionlevels-method"></a>IWMDRMLicense::GetOutputProtectionLevels-Methode

Die **GetOutputProtectionLevels-Methode** ruft Informationen zu allen Ausgabeschutzebenen (OUTPUT Protection Levels, OPLs) ab, die der Lizenz zugewiesen sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetOutputProtectionLevels(
  [out] WMDRM_OUTPUT_PROTECTION_LEVELS *pOPLs
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOPLs* \[ out\]
</dt> <dd>

Zeiger auf eine [**WMDRM \_ OUTPUT PROTECTION \_ \_ LEVELS-Struktur,**](wmdrm-output-protection-levels.md) die die OPL-Informationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMLicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





