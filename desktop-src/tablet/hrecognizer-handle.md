---
description: Ein HRECOGNIZER-Handle wird verwendet, um einen Erkennungskontext zu erstellen, die Attribute und Eigenschaften der Erkennung abzurufen und zu bestimmen, welche Paketeigenschaften die Erkennung für die Erkennung benötigt.
ms.assetid: 1fc1901e-8c4d-4ef1-8c38-52d46ce10a48
title: HRECOGNIZER-Handle (Recapis.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 192890991dcb7e8b0a0086bbca68a6ccbc2af790d9c7d78e76fe963d268c8240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092450"
---
# <a name="hrecognizer-handle"></a>HRECOGNIZER-Handle

Ein **HRECOGNIZER-Handle** wird verwendet, um einen Erkennungskontext zu erstellen, die Attribute und Eigenschaften der Erkennung abzurufen und zu bestimmen, welche Paketeigenschaften die Erkennung für die Erkennung benötigt.


```C++
typedef HANDLE HRECOGNIZER;
```



## <a name="remarks"></a>Hinweise

Die folgenden Funktionen verwenden **HRECOGNIZER**.



| Funktion                                                               | Beschreibung                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**CreateRecognizer**](/windows/desktop/api/recapis/nf-recapis-createrecognizer)                           | Erstellt eine Erkennung.<br/>                                                                   |
| [**DestroyRecognizer**](/windows/desktop/api/recapis/nf-recapis-destroyrecognizer)                         | Zerstört eine Erkennung.<br/>                                                                  |
| [**GetRecoAttributes**](/windows/desktop/api/recapis/nf-recapis-getrecoattributes)                         | Gibt die Attribute der Erkennung zurück.<br/>                                               |
| [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext)                                 | Erstellt einen Erkennungskontext.<br/>                                                           |
| [**DestroyContext**](/windows/desktop/api/recapis/nf-recapis-destroycontext)                               | Zerstört einen Erkennungskontext.<br/>                                                          |
| [**GetAllRecognizers**](/windows/desktop/api/recapis/nf-recapis-getallrecognizers)                         | Ruft alle Erkennungen ab.<br/>                                                                   |
| [**GetResultPropertyList**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)                 | Ruft eine Liste der Eigenschaften ab, die die Erkennung für einen Ergebnisbereich zurückgeben kann.<br/>            |
| [**GetPreferredPacketDescription**](/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription) | Ruft eine Paketbeschreibung ab, die die paketeigenschaften enthält, die von der Erkennung verwendet werden.<br/> |
| [**GetUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getunicoderanges)                           | Ruft die Bereiche von Unicode-Punkten ab, die die Erkennung unterstützt.<br/>                    |
| [**LoadCachedAttributes**](/windows/desktop/api/recapis/nf-recapis-loadcachedattributes)                   | Lädt die zwischengespeicherten Attribute einer Erkennung.<br/>                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Recapis.h</dt> </dl> |



 

 




