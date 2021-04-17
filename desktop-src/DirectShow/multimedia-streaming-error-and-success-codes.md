---
description: Multimediastreaming-Fehler und Erfolgs Codes
ms.assetid: 3b7a11d2-55b9-4505-8eb2-46be423c662b
title: Multimediastreaming-Fehler und Erfolgs Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54a185b46134f4603c7adea0f1b4467da3a2cf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351698"
---
# <a name="multimedia-streaming-error-and-success-codes"></a>Multimediastreaming-Fehler und Erfolgs Codes

> [!Note]  
> Diese API ist veraltet. Diese sollten von neuen Anwendungen nicht verwendet werden.

 

Die folgende Liste enthält Fehlermeldungen und Erfolgs Benachrichtigungen für Anwendungen, die die multimediastreaming-Schnittstellen verwenden. Diese Liste enthält nicht alle möglichen Fehler. Die angezeigten Fehler gelten speziell für die Microsoft® DirectShow-® Implementierung der multimediastreaming-Schnittstellen.



| Wert                       | Hexadezimalcode | BESCHREIBUNG                                                                                                                                                                                |
|-----------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ausstehende MS S \_              | 0x00040001       | Das Beispiel Update ist noch nicht fertiggestellt.                                                                                                                                                         |
| MS \_ S \_ noUpdate             | 0x00040002       | Das Beispiel wurde nach dem erzwungenen Abschluss nicht aktualisiert.                                                                                                                                            |
| MS \_ S \_ EndOf-Stream          | 0x00040003       | Ende des Datenstroms. Das Beispiel wurde nicht aktualisiert.                                                                                                                                                         |
| MS \_ E \_ samplezuzuweisung          | 0x80040401       | Ein [**imediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) -Objekt konnte nicht aus einem [**imultimediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) -Objekt entfernt werden, weil es immer noch mindestens ein zugeordneter Beispiel enthält. |
| MS \_ E \_ purposeid            | 0x80004005       | Die angegebene Zweck-ID kann nicht für den-Befehl verwendet werden.                                                                                                                                       |
| MS \_ E \_ nostream             | 0x80040403       | Es wurde kein Datenstrom mit den angegebenen Attributen gefunden.                                                                                                                                      |
| MS \_ E- \_ Suche            | 0x80040404       | Die Suche wird für dieses [**imultimediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) -Objekt nicht unterstützt.                                                                                                      |
| MS \_ E nicht \_ kompatibel         | 0x80040405       | Die Streamformate sind nicht kompatibel.                                                                                                                                                     |
| MS \_ E \_ ausgelastet                 | 0x80040406       | Das Beispiel ist ausgelastet.                                                                                                                                                                        |
| MS \_ E \_ notinit              | 0x80040407       | Das Objekt kann den Aufruf nicht akzeptieren, weil die Initialisierungsfunktion oder die entsprechende Funktion nicht aufgerufen wurde.                                                                                        |
| MS \_ E \_ sourceallesdefined | 0x80040408       | Die Quelle ist bereits definiert.                                                                                                                                                                    |
| MS \_ E \_ invalidstreamtype    | 0x80040409       | Der Streamtyp ist für diesen Vorgang ungültig.                                                                                                                                           |
| MS \_ E \_ notrunning           | 0x8004040a       | Das [**imultimediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) -Objekt befindet sich nicht im Status "wird ausgeführt".                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Multimediarestreaming](multimedia-streaming.md)
</dt> </dl>

 

 



