---
description: Die Kommunikation umfasst häufig potenziell große Datenmengen oder Daten unbekannter Länge.
ms.assetid: e7b12b9e-8caa-4dad-b81f-b609ccb92c9f
title: Verwenden von SecBufferDesc und SecBuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ad12120414a1e0acb7a6b1cfe211b0ed1787d9e676e8329df1e16ecfef17cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785910"
---
# <a name="using-secbufferdesc-and-secbuffer"></a>Verwenden von SecBufferDesc und SecBuffer

Die Kommunikation umfasst häufig potenziell große Datenmengen oder Daten unbekannter Länge. Das Senden und Empfangen von Daten erfolgt in beiden Fällen auf ähnliche oder identische Weise. Für den Umgang mit unbekannter Länge und potenziell großen Datenmengen erfolgt die SSPI-Kommunikation mithilfe der beiden Strukturen [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) und [**SecBuffer.**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)

Eine [**SecBufferDesc-Struktur**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) ist ein Container für ein Array von [**SecBuffer-Strukturen.**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) Eine **SecBufferDesc-Struktur** verfügt über die folgenden Member:

-   Versionsnummer
-   Anzahl von [**SecBuffer-Elementen**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)
-   Adresse des Arrays von [**SecBuffer-Strukturen**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)

Eine [**SecBuffer-Struktur**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) enthält die folgenden drei Member:

-   Anzahl der Bytes im Puffer
-   Typ der im Datenelement enthaltenen Informationen
-   Die Bytes selbst

Eine gesamte SSPI-Nachricht besteht häufig aus einem Array von [**SecBuffer-Strukturen.**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)

Die folgenden Pufferdatentypen sind wie folgt definiert.



| Puffertyp                | Bedeutung                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| SECBUFFER \_ EMPTY           | Nicht definiert, ersetzt durch die [*Sicherheitspaketfunktion*](../secgloss/s-gly.md) |
| \_SECBUFFER-DATEN            | Paketdaten                                                                                                                            |
| SECBUFFER-TOKEN \_           | Sicherheitstoken                                                                                                                         |
| \_SECBUFFER-PKG-PARAMS \_     | Paketspezifische Parameter                                                                                                            |
| SECBUFFER \_ FEHLT         | Fehlender Datenindikator                                                                                                                 |
| SECBUFFER \_ EXTRA           | Zusätzliche Daten                                                                                                                             |
| SECBUFFER \_ STREAM          | Sicherheitsstreamdaten                                                                                                                   |
| SECBUFFER \_ STREAM \_ TRAILER | Sicherheitsstream-Nachspann                                                                                                                |
| \_SECBUFFER-STREAMHEADER \_  | Sicherheitsstreamheader                                                                                                                 |



 

Die oben genannten Puffertypen können mithilfe einer bitweise-OR-Operation mit einem der folgenden Puffertypen kombiniert werden.



| Puffertyp         | Bedeutung                                                                          |
|---------------------|----------------------------------------------------------------------------------|
| SECBUFFER \_ ATTRMASK | Maskieren Sie Sicherheitsattribute, indem Sie die Attributflags vom Puffertyp trennen. |
| SECBUFFER \_ READONLY | Puffer ist schreibgeschützt                                                              |



 

Vor jedem Aufruf einer SSPI-API, die einen [**SecBufferDesc-Parameter**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) erfordert, werden mindestens ein [**SecBuffer-Array-Element**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) deklariert und initialisiert. Beispielsweise kann es zwei Sicherheitspuffer geben: einen, der Eingabenachrichtendaten enthält, und den anderen für das nicht transparente Ausgabesicherheitstoken, das vom Sicherheitspaket zurückgegeben wird. Die Reihenfolge der Sicherheitspuffer im Sicherheitspufferdeskriptor ist nicht wichtig, aber jeder Puffer muss mit dem entsprechenden Typ gekennzeichnet werden. Ein schreibgeschütztes Tag kann mit jedem Eingabepuffer verwendet werden, der nicht vom Sicherheitspaket [*geändert werden darf.*](../secgloss/s-gly.md)

Die Größe des Ausgabepuffers, der das Sicherheitstoken enthalten soll, ist wichtig. Eine Anwendung kann die maximale Tokengröße für ein Sicherheitspaket während der ersten Einrichtung finden. Der Aufruf von [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) gibt ein Array von Zeigern auf Sicherheitspaketinformationen zurück. Die Sicherheitspaket-Informationsstruktur enthält die maximale Tokengröße für jedes Paket. Im Beispiel sind die Informationen im **cbMaxToken-Member** der [**SecPkgInfo-Struktur**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) enthalten. Die gleichen Informationen können später mithilfe von [**QuerySecurityPackageInfo ermittelt werden.**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa)

Die Anwendung initialisiert die Pufferzeker und -größen in der Pufferbeschreibung, um anzugeben, wo Nachrichtendaten und andere Informationen gefunden werden können.

Weitere Informationen finden Sie unter [SecBuffer- und SecBufferDesc-Beispielcode.](secbuffer-and-secbufferdesc-example-code.md)

 

 
