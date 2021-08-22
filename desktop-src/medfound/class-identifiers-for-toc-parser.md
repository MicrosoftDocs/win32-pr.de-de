---
description: Die folgenden Klassen werden deklariert und klassenbezeichnern (CLSIDs) in wmcodecdsp.h zugeordnet.
ms.assetid: f82d92dc-fbce-4274-a10f-72fa8dd776cc
title: Klassenbezeichner für den Inhaltsverzeichnisparser (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c340ec32b8de4ce42619d57f6e44da9d77d0eead4940dc94d90baec4d349ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664690"
---
# <a name="class-identifiers-for-table-of-contents-parser"></a>Klassenbezeichner für den Inhaltsverzeichnisparser

Die folgenden Klassen werden deklariert und klassenbezeichnern (CLSIDs) in wmcodecdsp.h zugeordnet.



| Klassenname       | Anzeigeobjektname |
|------------------|----------------------|
| CTocEntry        | TOC-Eintrag            |
| CTocEntryList    | TOC-Eintragsliste       |
| CToc             | INHALTSVERZEICHNIS                  |
| CTocCollection   | TOC-Sammlung       |
| CTocParser       | TOC-Parser           |
| CTocGeneratorDmo | TOC Generator        |



 

Die obige Tabelle enthält einen Anzeigeobjektnamen für jede Klasse. In dieser Dokumentation werden diese Anzeigenamen verwendet, um auf Instanzen der Klassen zu verweisen. Die Dokumentation bezieht sich beispielsweise auf eine Instanz der CTocEntry-Klasse als TOC Entry-Objekt.

Im Code können Sie **\_ \_ uuidof** verwenden, um auf die CLSIDs zu verweisen. Beispielsweise können Sie den folgenden Code verwenden, um auf die CLSID für CTocGeneratorDmo zu verweisen.


```C++
__uuidof(CTocGeneratorDmo)
```



### <a name="clsid-constants-defined-in-wmcodecdsph"></a>CLSID-Konstanten, die in Wmcodecdsp.h definiert sind

Als Alternative zur Verwendung von **\_ \_ uuidof** können Sie Konstanten verwenden, um auf die CLSIDs zu verweisen. Die folgenden Konstanten sind in wmcodecdsp.h definiert.



| Klassenname     | CLSID-Konstante        |
|----------------|-----------------------|
| CTocEntry      | CLSID \_ CTocEntry      |
| CTocEntryList  | CLSID \_ CTocEntryList  |
| CToc           | CLSID \_ CToc           |
| CTocCollection | CLSID \_ CTocCollection |
| CTocParser     | CLSID \_ CTocParser     |



 

### <a name="clsid-constants-defined-in-wmcodecdspuuidlib"></a>CLSID-Konstanten definiert in Wmcodecdspuuid.lib

Die folgende CLSID-Konstante wird in wmcodecdsp.h deklariert, aber nicht definiert. Um sie im Code zu verwenden, müssen Sie eine Verknüpfung mit wmcodecdspuuid.lib erstellen.



| Klassenname       | CLSID-Konstante          |
|------------------|-------------------------|
| CTocGeneratorDmo | CLSID \_ CTocGeneratorDmo |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmvdspa.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Inhaltsverzeichnisparserobjekte](toc-parser-objects.md)
</dt> </dl>

 

 




