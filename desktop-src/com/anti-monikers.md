---
title: Anti-Moniker
description: OLE stellt eine Implementierung eines besonderen Typs von Moniker bereit, der als Anti-Moniker bezeichnet wird.
ms.assetid: 3b52d3bd-8375-4463-a0e3-5117fa96a1c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d69c461268b486a040b36f59108bc8e8379656
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037101"
---
# <a name="anti-monikers"></a>Anti-Moniker

OLE stellt eine Implementierung eines besonderen Typs von Moniker bereit, der als *Anti-Moniker* bezeichnet wird. Dieser Moniker wird bei der Erstellung neuer Monikerklassen verwendet. Sie verwenden Sie als Umkehrung des Monikers, auf dem Sie erstellt wurde, und den Moniker effektiv abbrechen, ähnlich wie der Operator ".." in einem Dateisystem Befehl eine Verzeichnisebene verschiebt.

Es muss ein-antimoniker verfügbar sein, da nach dem Erstellen eines zusammengesetzten Monikers keine Teile des Monikers gelöscht werden können, wenn z. b. ein-Objekt verschoben wird. Stattdessen verwenden Sie einen-antimoniker, um einen oder mehrere Einträge aus einem zusammengesetzten Moniker zu entfernen.

Anti-Moniker sind eine Monikerklasse, die explizit für die Verwendung als Umkehrung vorgesehen ist. COM definiert die benannte Funktion " [**comateantimoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) ", die einen Anti-Moniker zurückgibt. Im Allgemeinen verwenden Sie diese Funktion, um die [**IMoniker:: inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) -Methode zu implementieren.

Ein Anti-Moniker ist nur eine Umkehrung für die Typen von Monikern, die implementiert werden, um antimoniker als Umkehrung zu behandeln. Wenn Sie z. b. den letzten Teil eines zusammengesetzten Monikers entfernen möchten, sollten Sie keinen antimoniker erstellen und ihn am Ende der zusammengesetzten zusammensetzen. Sie können nicht sicher sein, dass der letzte Teil des zusammengesetzten einen antimoniker als Umkehrung ansieht. Stattdessen sollten Sie [**IMoniker:: Enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) für den zusammengesetzten Moniker aufrufen und dabei **false** als ersten Parameter angeben. Dadurch wird ein Enumerator erstellt, der die komponentenmoniker in umgekehrter Reihenfolge zurückgibt. Verwenden Sie den Enumerator, um den letzten Teil des zusammengesetzten abzurufen, und rufen Sie [**inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) für diesen Moniker auf. Der von **inverse** zurückgegebene Moniker ist das, was Sie benötigen, um den letzten Teil des zusammengesetzten zu entfernen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Klassenmoniker](class-monikers.md)
</dt> <dt>

[Zusammengesetzte Moniker](composite-monikers.md)
</dt> <dt>

[Dateimoniker](file-monikers.md)
</dt> <dt>

[Elementmoniker](item-monikers.md)
</dt> <dt>

[Zeigermoniker](pointer-monikers.md)
</dt> </dl>

 

 




