---
description: Ein herkenzer-Handle wird verwendet, um einen Erkennungs Kontext zu erstellen, die Attribute und Eigenschaften der Erkennungsfunktion abzurufen und zu bestimmen, welche Paket Eigenschaften die Erkennung zum Durchführen der Erkennung benötigt.
ms.assetid: 1fc1901e-8c4d-4ef1-8c38-52d46ce10a48
title: Herkenzer-handle ("recapis. h")
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e78086ff86453ef8b0157bb3b274f3c47be0dc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343748"
---
# <a name="hrecognizer-handle"></a>Herkenzer-handle

Ein **herkenzer** -Handle wird verwendet, um einen Erkennungs Kontext zu erstellen, die Attribute und Eigenschaften der Erkennungsfunktion abzurufen und zu bestimmen, welche Paket Eigenschaften die Erkennung zum Durchführen der Erkennung benötigt.


```C++
typedef HANDLE HRECOGNIZER;
```



## <a name="remarks"></a>Bemerkungen

Die folgenden Funktionen verwenden einen **herkenzer**.



| Funktion                                                               | BESCHREIBUNG                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**"Kreaterecognizer"**](/windows/desktop/api/recapis/nf-recapis-createrecognizer)                           | Erstellt eine Erkennung.<br/>                                                                   |
| [**Destroyerkenzer**](/windows/desktop/api/recapis/nf-recapis-destroyrecognizer)                         | Zerstört eine Erkennung.<br/>                                                                  |
| [**Getrecoattribute**](/windows/desktop/api/recapis/nf-recapis-getrecoattributes)                         | Gibt die Attribute des Erkennungs Moduls zurück.<br/>                                               |
| [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext)                                 | Erstellt einen Erkennungs Kontext.<br/>                                                           |
| [**Destroycontext**](/windows/desktop/api/recapis/nf-recapis-destroycontext)                               | Zerstört einen Erkennungs Kontext.<br/>                                                          |
| [**Getallerkenzers**](/windows/desktop/api/recapis/nf-recapis-getallrecognizers)                         | Ruft alle erkenzer ab.<br/>                                                                   |
| [**Getresultpropertylist**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)                 | Ruft eine Liste von Eigenschaften ab, die die Erkennung für einen Ergebnisbereich zurückgeben kann.<br/>            |
| [**Getpreferredpacketdescription**](/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription) | Ruft eine Paketbeschreibung ab, die die Paket Eigenschaften enthält, die die Erkennung verwendet.<br/> |
| [**GetUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getunicoderanges)                           | Ruft die Bereiche von Unicode-Punkten ab, die von der Erkennung unterstützt werden.<br/>                    |
| [**Loadcachedattributes**](/windows/desktop/api/recapis/nf-recapis-loadcachedattributes)                   | Lädt die zwischengespeicherten Attribute einer Erkennung.<br/>                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>"Recapis. h"</dt> </dl> |



 

 




