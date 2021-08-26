---
description: Die Persist-Methode des SummaryInfo-Objekts formatiert und schreibt die zuvor gespeicherten Eigenschaften in den standardmäßigen SummaryInformation-Stream.
ms.assetid: 77ec1754-73b1-416e-9c9d-72fdbabe16ae
title: SummaryInfo.Persist-Methode
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
ms.openlocfilehash: 35916dccc3b131d49176b4ecc1a31fedf40c7c5eafeb4c107b30de08db21dc81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039600"
---
# <a name="summaryinfopersist-method"></a>SummaryInfo.Persist-Methode

Die **Persist-Methode** des [**SummaryInfo-Objekts**](summaryinfo-object.md) formatiert und schreibt die zuvor gespeicherten Eigenschaften in den standardmäßigen SummaryInformation-Stream. Es wird ein Fehler generiert, wenn der Stream nicht erfolgreich geschrieben werden kann. Diese Methode kann nur einmal aufgerufen werden, nachdem alle Eigenschaftswerte festgelegt wurden. Eigenschaften können weiterhin gelesen werden, nachdem der Stream geschrieben wurde.

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
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo ist als 000C109B-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                         |



 

 




