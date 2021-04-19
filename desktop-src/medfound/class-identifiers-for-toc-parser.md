---
description: Die folgenden Klassen werden deklariert und mit Klassen Bezeichner (CLSIDs) in wmcodecdsp. h verknüpft.
ms.assetid: f82d92dc-fbce-4274-a10f-72fa8dd776cc
title: Klassen Bezeichner für den Inhaltsverzeichnis Tabelle (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5108855c687085e77ce36aa14b3424732e25572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346670"
---
# <a name="class-identifiers-for-table-of-contents-parser"></a>Klassen Bezeichner für Inhaltsverzeichnis Tabelle

Die folgenden Klassen werden deklariert und mit Klassen Bezeichner (CLSIDs) in wmcodecdsp. h verknüpft.



| Klassenname       | Anzeigeobjekt Name |
|------------------|----------------------|
| Cchcentry        | Inhaltseintrag            |
| Cycentrylist    | Inhaltsliste für Inhaltsverzeichnis       |
| Cinhalts Verzeichnis             | INHALTSVERZEICHNIS                  |
| Cdeccollection   | Inhalts Sammlung       |
| Cdecparser       | Inhaltsverzeichnis           |
| Cdecgeneratordmo | TOC-Generator        |



 

Die obige Tabelle enthält einen anzeigen Amen für jede Klasse. In dieser Dokumentation werden diese anzeigen Amen verwendet, um auf Instanzen der Klassen zu verweisen. Die Dokumentation bezieht sich z. b. auf eine Instanz der cycentry-Klasse als ein Inhalts Objekt.

Im Code können Sie **\_ \_ uuidof** verwenden, um auf die CLSIDs zu verweisen. Beispielsweise können Sie den folgenden Code verwenden, um auf die CLSID für cycgeneratordmo zu verweisen.


```C++
__uuidof(CTocGeneratorDmo)
```



### <a name="clsid-constants-defined-in-wmcodecdsph"></a>In "wmcodecdsp. h" definierte CLSID-Konstanten

Als Alternative zur Verwendung von **\_ \_ uuidof** können Sie Konstanten verwenden, um auf die CLSIDs zu verweisen. Die folgenden Konstanten sind in wmcodecdsp. h definiert.



| Klassenname     | CLSID-Konstante        |
|----------------|-----------------------|
| Cchcentry      | CLSID \_ cumcentry      |
| Cycentrylist  | CLSID \_ cycentrylist  |
| Cinhalts Verzeichnis           | CLSID- \_ cinhalts           |
| Cdeccollection | CLSID \_ cdeccollection |
| Cdecparser     | CLSID \_ cdecparser     |



 

### <a name="clsid-constants-defined-in-wmcodecdspuuidlib"></a>In wmcodecdspuuid. lib definierte CLSID-Konstanten

Die folgende CLSID-Konstante wird in wmcodecdsp. h deklariert, aber nicht definiert. Um Sie im Code zu verwenden, müssen Sie eine Verknüpfung mit wmcodecdspuuid. lib herstellen.



| Klassenname       | CLSID-Konstante          |
|------------------|-------------------------|
| Cdecgeneratordmo | CLSID \_ cdecgeneratordmo |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmvdspa.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Tabelle mit Inhalts parserobjekten](toc-parser-objects.md)
</dt> </dl>

 

 




