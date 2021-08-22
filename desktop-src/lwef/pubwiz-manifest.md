---
title: Verwenden des Übertragungsmanifests
description: Der Webveröffentlichungs-Assistent und der Onlinedruckreihenfolge-Assistent verwenden das Übertragungsmanifest, um Details zur Datenübertragung zwischen dem Clientcomputer und dem Serverstandort zu kommunizieren.
ms.assetid: b7bb541c-3bf4-4aab-ac70-c006517e772e
keywords:
- Webveröffentlichungs-Assistent,Übertragungsmanifest
- Onlinedruckreihenfolge-Assistent,Übertragungsmanifest
- Übertragungsmanifest
- manifest
- window.external,Übertragungsmanifest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d7f4ea3f9cd392f4b0bab50e1e558613fc7485d4f44a27472cd48ad898b3ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555850"
---
# <a name="using-the-transfer-manifest"></a>Verwenden des Übertragungsmanifests

Der Webveröffentlichungs-Assistent und der Onlinedruckreihenfolge-Assistent verwenden das Übertragungsmanifest, um Details zur Datenübertragung zwischen dem Clientcomputer und dem Serverstandort zu kommunizieren.

## <a name="the-purpose-of-the-transfer-manifest"></a>Zweck des Übertragungsmanifests

Das Übertragungsmanifest beschreibt dateien, die an der Übertragung beteiligt sind, einschließlich Details wie die Zielhierarchie und die Metadaten der Datei. Serverseitige Skripts können das Manifest ändern, indem ungeeignete Dateien aus der Liste entfernt und Informationen dazu hinzugefügt werden, wie und wo die Dateien übertragen werden sollen.

Das Manifest wird als **Eigenschaftendokument window.external.Property("TransferManifest")** verfügbar gemacht, ein DOM-Dokument (XML Dokumentobjektmodell). Weitere Informationen zum XML-DOM finden Sie in der MSDN-Dokumentation für [IXMLDOMDocument/DOMDocument.](/previous-versions/windows/desktop/ms756987(v=vs.85))

Die Organisation des Übertragungsmanifests auf oberster Ebene sieht wie folgt aus:


```
<transfermanifest>
    <filelist/>
    <folderlist/>
    <uploadinfo/>
</transfermanifest>
```



Die serverseitige HTML-Seite kann die Knoten im Manifest verwenden, um bestimmte Informationen zu den zu kopierenden Dateien abzurufen und dann die Benutzeroberfläche des Diensts entsprechend zu ändern. Beispielsweise kann eine Fotodruckwebsite die Informationen verwenden, um Miniaturansichten der ausgewählten Bilder anzuzeigen, während eine Speicherwebsite die Informationen verwenden kann, um sicherzustellen, dass genügend Speicherplatz für diesen Benutzer verfügbar ist. Vollständige Informationen zu den Knoten und Attributen des Übertragungsmanifests finden Sie unter Übertragen des [Manifestschemas.](/windows/desktop/shell/interfaces)

Das Schema des Übertragungsmanifests wird als offenes Modell geschrieben, sodass Elemente, die nicht speziell im Schema definiert sind, im Übertragungsmanifest angezeigt werden können. Daher kann eine Anbieterwebsite proprietäre Elemente für die eigene Verwendung hinzufügen, ohne die Gültigkeit des Manifests zu beeinträchtigen. Das Schema wird auch so definiert, dass die Reihenfolge der Elemente nicht eingeschränkt wird.

> [!Note]  
> Das Manifest wird jedes Mal neu erstellt, wenn ein neuer Anbieter ausgewählt wird, sodass der Anbieter Standortinformationen im Manifest speichern kann.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übertragen des Manifestschemas](/windows/desktop/shell/interfaces)
</dt> </dl>

 

 