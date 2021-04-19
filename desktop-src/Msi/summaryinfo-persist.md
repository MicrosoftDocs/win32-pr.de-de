---
description: Die Persistenzmethode des SummaryInfo-Objekts formatiert und schreibt die zuvor gespeicherten Eigenschaften in den standardmäßigen SummaryInformation-Stream.
ms.assetid: 77ec1754-73b1-416e-9c9d-72fdbabe16ae
title: SummaryInfo. persistent-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Persist
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e454631e27476e6d18b85908f651d89c2e8063ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361305"
---
# <a name="summaryinfopersist-method"></a>SummaryInfo. persistent-Methode

Die **Persistenzmethode** des [**SummaryInfo**](summaryinfo-object.md) -Objekts formatiert und schreibt die zuvor gespeicherten Eigenschaften in den standardmäßigen SummaryInformation-Stream. Es wird ein Fehler generiert, wenn der Stream nicht erfolgreich geschrieben werden kann. Diese Methode kann nur einmal aufgerufen werden, nachdem alle Eigenschaftswerte festgelegt wurden. Eigenschaften können nach dem Schreiben des Streams noch gelesen werden.

## <a name="syntax"></a>Syntax


```JScript
SummaryInfo.Persist()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ isummaryinfo ist definiert als 000c109b-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



 

 




