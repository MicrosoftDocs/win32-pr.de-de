---
title: Implementierung von idirectschreiterlock-Verbund Dateien
description: Die Implementierung der Verbund Datei von idirectschreiterlock bietet eine Möglichkeit zum Öffnen einer Verbund Datei im direkten Modus mit einem einzigen Writer und mehreren Lesern.
ms.assetid: 4b247dae-d937-430a-bdb7-c47fa3c026b6
keywords:
- Idirectwrite terlock-geg, Implementierung von Verbund Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 861935a4c373ce03408c0e633e581e56d39623da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708453"
---
# <a name="idirectwriterlock---compound-file-implementation"></a>Implementierung von idirectschreiterlock-Verbund Dateien

Die Implementierung der Verbund Datei von [**idirectschreiterlock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) bietet eine Möglichkeit zum Öffnen einer Verbund Datei im direkten Modus mit einem einzigen Writer und mehreren Lesern.

Verbund Dateien können im direkt Modus mit dem STGM Direct- \_ Flag geöffnet werden. Die [**idirectschreiterlock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) -Schnittstelle legt das STGM- \_ \| Schreib kennflag "Read Write STGM" \_ \_ \_ als gültig im direkten Modus fest, ohne dass der Aufwand einer Momentaufnahme Kopie erforderlich ist.

Wenn eine Verbund Datei mit dem transaktiven STGM-Flag im transaktiven Modus geöffnet wird \_ , können Sie auch mehrere Reader und einen einzigen Writer verwenden, indem Sie das kennflag zum Schreiben von "STGM" für "read \_ Write \| STGM" verwenden \_ \_ \_ . In diesem Fall wird jedoch eine Momentaufnahme Kopie der Datei für die Leser erstellt. Der Aufwand für eine Scratch-Kopie ist häufig zu erhöhen.

## <a name="when-to-use"></a>Verwendungs Zeitpunkt

Verwenden Sie die vom System bereitgestellte Implementierung von [**idirectschreiterlock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) , wenn Sie einen Speicher im direkten Modus (STGM \_ Direct) mit der STGM-Schreib Schreib-/Schreib-Schreib-Kennzeichnungen für den STGM- \_ Lesevorgang \| \_ \_ \_

Rufen Sie zum Abrufen eines Zeigers auf [**idirectschreiterlock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) **QueryInterface** für [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) auf, um das Stamm Speicher Objekt für die Verbund Datei abzurufen.

Rufen Sie [**idirectschreiterlock:: waitforschreiteaccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) auf, um exklusiven Schreibzugriff auf eine Verbund Datei zu erhalten. Aufrufen von [**idirectschreiterlock:: releaseschreiteaccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-releasewriteaccess) , um exklusiven Schreibzugriff freizugeben.

[**Idirectschreiterlock:: haveschreiteaccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-havewriteaccess) gibt an, ob die Datei zurzeit gesperrt ist.

## <a name="remarks"></a>Bemerkungen

Die Implementierung der Verbund Datei des Single Writer-Features mit mehreren Lese Vorlesern basiert auf Bereichs sperren. Der Writer erhält exklusiven Zugriff auf den zu schreibende Speicher, nachdem alle aktuellen Reader den Speicher geschlossen haben. Während der Writer aktiv ist, können nachfolgende Reader den Speicher nicht öffnen. Der Writer ruft [**idirectbeschreib terlock:: waitforschreiteaccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) auf, um exklusiven Schreibzugriff zu erhalten. Der Writer muss dann " [**idirectschreiterlock:: releaseschreiteaccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-releasewriteaccess) " aufrufen, um den Speicher freizugeben.

Der Aufrufen von [**idirectwriterlock:: waitforwriteaccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) ist vor dem Schreiben in diesem Single Reader-, Multiple Writer-Modus erforderlich. Versucht, in die Datei zu schreiben, ohne **idirectbeschreib terlock:: waitforschreiteaccess** zuerst aufrufen zu können \_ \_ . Dieser Fehler wird auch dann zurückgegeben, wenn der Writer die Datei anfänglich geöffnet hat und derzeit keine Datei geöffnet ist.

## <a name="marshaling-considerations"></a>Überlegungen zu Marshalling

Das benutzerdefinierte Marshalling wird normalerweise verwendet, wenn eine Verbund Datei an einen anderen Prozess auf demselben Computer gemarshallt wird. Beim Marshalling von Speicher werden keine Zugriffsrechte berücksichtigt, und der [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Zeiger wird an den neuen Prozess mit denselben Zugriffs Modi und denselben Zugriffs Modi wie der ursprüngliche Marshallingprozess übermittelt. Weitere Informationen zu Zugriffs Modi finden Sie unter [**STGM-Konstanten**](stgm-constants.md). Beim Marshalling werden keine Sperren erstellt oder überprüft, um exklusiven Schreibzugriff sicherzustellen. In diesem Fall gibt es keine Erzwingung der Richtlinie für den einzelnen Writer für Verbund Dateien, die im Single Writer-Modus (mehrfach Lese Modus) geöffnet sind. Stattdessen wird die Erzwingung intern von der Implementierung der Verbund Datei verarbeitet.

Da der [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Zeiger während des Marshalling an einen anderen Prozess übermittelt wird, kann es vorkommen, dass zwei Prozesse gleichzeitig auf dieselbe Verbund Datei zugreifen können. Obwohl ein Aufrufer exklusiven Schreibzugriff auf den Speicher erhalten hat, indem er [**idirectbeschreib terlock:: waitforschreiteaccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess)aufgerufen hat, kann die gemarshallte Version auch gleichzeitig Zugriff haben. Die gemarshallten Versionen müssen nicht geschlossen werden, während der einzelne Writer auf die Datei zugreift. In diesem Fall synchronisiert die Implementierung der Verbund Datei die Schreibvorgänge intern.

Wenn ein einzelner Writer exklusiven Zugriff erhält, indem er, [**idirectschreiterlock:: waitforschreiteaccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess)aufruft, verfügt der gemarshallte Speicher auch über Schreibzugriff und muss nicht **idirectschreiterlock:: waitforschreiteaccess** aufrufen. Beide Prozesse haben Schreibzugriff, und die Synchronisierung wird von der internen Implementierung der Verbund Datei gesteuert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Idirectschreiblock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock)
</dt> </dl>

 

 




