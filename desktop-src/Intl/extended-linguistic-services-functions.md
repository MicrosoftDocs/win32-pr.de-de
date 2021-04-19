---
description: Els unterstützt die in der folgenden Tabelle definierten Funktionen.
ms.assetid: d62ab664-a75a-4d06-aefb-a3311ea7d4a7
title: Erweiterte Funktionen für linguistische Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5b8acff7601955f8ed6e37f430caa0a52aa880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358543"
---
# <a name="extended-linguistic-services-functions"></a>Erweiterte Funktionen für linguistische Dienste

Els unterstützt die in der folgenden Tabelle definierten Funktionen.



| Funktion                                                 | BESCHREIBUNG                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Mappingcallbackproc**](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)       | Eine Anwendungs definierte Rückruffunktion, die Daten asynchron verarbeitet, die von der **mappingrecognizetext** -Funktion erzeugt werden.                 |
| [**Mappingdoaction**](/windows/desktop/api/Elscore/nf-elscore-mappingdoaction)               | Bewirkt, dass ein Els-Dienst eine Aktion ausführt, nachdem die Texterkennung aufgetreten ist.                                                                |
| [**Mappingfrepropertybag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) | Gibt Arbeitsspeicher und Ressourcen frei, die während eines Els-Text Erkennungs Vorgangs zugeordnet werden.                                                                 |
| [**Mappingfreeservices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)       | Gibt Arbeitsspeicher und Ressourcen frei, die der Anwendung für die Interaktion mit einem oder mehreren Els-Diensten zugeordnet sind.                                            |
| [**Mappinggetservices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)         | Ruft nach den von der Anwendung angegebenen Kriterien eine Liste der verfügbaren, von der Plattform unterstützten Dienste zusammen mit zugeordneten Informationen ab. |
| [**Mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)     | Ruft auf einem Els-Dienst auf, um Text zu erkennen.                                                                                                   |



 

 

 



