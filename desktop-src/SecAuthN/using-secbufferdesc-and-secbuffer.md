---
description: Die Kommunikation umfasst häufig große Datenmengen oder Daten mit unbekannter Länge.
ms.assetid: e7b12b9e-8caa-4dad-b81f-b609ccb92c9f
title: Verwenden von secbufferde SC und secbuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ca7d8155a610263838d2baf2a7d1c8fc96ec874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867236"
---
# <a name="using-secbufferdesc-and-secbuffer"></a>Verwenden von secbufferde SC und secbuffer

Die Kommunikation umfasst häufig große Datenmengen oder Daten mit unbekannter Länge. Das Senden und empfangen von Daten erfolgt in beiden Fällen ähnlich oder identisch. Für den Umgang mit unbekannter Länge und potenziell großen Datenmengen erfolgt die SSPI-Kommunikation mithilfe der beiden Strukturen [**secbufferdesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) und [**secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer).

Eine [**secbufferdebug**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) -Struktur ist ein Container für ein Array von [**secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) -Strukturen. Eine **secbufferdebug** -Struktur verfügt über die folgenden Member:

-   Versionsnummer
-   Anzahl der [**secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) -Elemente
-   Adresse des Arrays der [**secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) -Strukturen

Eine [**secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) -Struktur enthält die folgenden drei Elemente:

-   Anzahl von Bytes im Puffer
-   Der Typ der Informationen, die im Datenelement enthalten sind.
-   Die Bytes selbst

Eine gesamte SSPI-Nachricht besteht häufig aus einem Array von [**secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) -Strukturen.

Die folgenden Puffer Datentypen werden wie folgt definiert.



| Puffertyp                | Bedeutung                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| secbuffer ist \_ leer.           | Nicht definiert, ersetzt durch die Funktion des [*Sicherheitspakets*](../secgloss/s-gly.md) |
| secbuffer- \_ Daten            | Paketdaten                                                                                                                            |
| secbuffer- \_ Token           | Sicherheits Token                                                                                                                         |
| secbuffer \_ pkg-Parameter \_     | Paket spezifische Parameter                                                                                                            |
| secbuffer \_ fehlt.         | Fehlender Daten Indikator                                                                                                                 |
| secbuffer- \_ Zusatz           | Zusätzliche Daten                                                                                                                             |
| secbuffer- \_ Stream          | Sicherheitsstreamdaten                                                                                                                   |
| secbuffer- \_ streamnachspann \_ | Sicherheitsstreamnachspann                                                                                                                |
| secbuffer \_ - \_ Streamheader  | Sicherheitsstreamheader                                                                                                                 |



 

Die Puffer Typen oben können mit einem bitweisen **or** -Vorgang mit einem der folgenden Puffer Typen kombiniert werden.



| Puffertyp         | Bedeutung                                                                          |
|---------------------|----------------------------------------------------------------------------------|
| secbuffer- \_ attrmask | Maskieren von Sicherheits Attributen Durchtrennen der Attributflags vom Puffertyp. |
| secbuffer \_ schreibgeschützt | Der Puffer ist schreibgeschützt.                                                              |



 

Vor jedem Aufrufen einer SSPI-API, die einen [**secbufferdesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) -Parameter erfordert, werden ein oder mehrere [**secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) -Array Elemente deklariert und initialisiert. Es können z. b. zwei Sicherheitspuffer vorhanden sein: eine mit Eingabe Nachrichten Daten und die andere für das vom Sicherheitspaket zurückgegebene, nicht transparente Sicherheits Token. Die Reihenfolge der Sicherheitspuffer im Sicherheitspuffer Deskriptor ist nicht wichtig, aber jeder Puffer muss mit dem entsprechenden Typ gekennzeichnet werden. Ein Schreib geschütztes-Tag kann mit jedem Eingabepuffer verwendet werden, der nicht vom [*Sicherheitspaket*](../secgloss/s-gly.md)geändert werden darf.

Die Größe des Ausgabepuffers, der das Sicherheits Token enthalten soll, ist wichtig. Eine Anwendung kann die maximale Tokengröße für ein Sicherheitspaket während des ersten Setups ermitteln. Der- [**enumeratesecuritypackages-Enumerationstyp**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) gibt ein Array von Zeigern auf Sicherheitspaket Informationen zurück. Die Struktur der Sicherheitspaket Informationen enthält die maximale Tokengröße für jedes Paket. In diesem Beispiel befinden sich die Informationen im **cbmaxtoken** -Member der [**secpkginfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) -Struktur. Die gleichen Informationen können später mithilfe von [**querysecuritypackageinfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa)abgerufen werden.

Die Anwendung initialisiert die Puffer Zeiger und-Größen in der Puffer Beschreibung, um anzugeben, wo Nachrichten Daten und andere Informationen gefunden werden können.

Weitere Informationen finden Sie unter [Beispiel Code für secbuffer und secbufferdesc](secbuffer-and-secbufferdesc-example-code.md).

 

 
