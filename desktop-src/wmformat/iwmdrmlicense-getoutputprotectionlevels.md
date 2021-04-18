---
title: Iwmdrmlicense getoutputschutzlevels-Methode
description: Die getoutputschutzlevels-Methode ruft Informationen zu allen Ausgabe Schutz Ebenen (opls) ab, die der Lizenz zugewiesen sind.
ms.assetid: 6596171a-67ac-42cd-80d9-f77507fc58eb
keywords:
- Getoutputschutzlevels-Methode Windows Media-Format
- Getoutputschutzlevels-Methode, Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, getoutputschutzlevels-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetOutputProtectionLevels
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5318ecdc8322699ac9d942425a98347799c37715
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338225"
---
# <a name="iwmdrmlicensegetoutputprotectionlevels-method"></a>Iwmdrmlicense:: getoutputschutzlevels-Methode

Die **getoutputschutzlevels** -Methode ruft Informationen zu allen Ausgabe Schutz Ebenen (opls) ab, die der Lizenz zugewiesen sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetOutputProtectionLevels(
  [out] WMDRM_OUTPUT_PROTECTION_LEVELS *pOPLs
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*popls* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine [**WMDRM- \_ Ausgabe \_ Schutz \_ Ebenen**](wmdrm-output-protection-levels.md) -Struktur, die die OPL-Informationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Iwmdrmlicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





