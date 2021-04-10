---
title: Verwenden des Übertragungs Manifests
description: Der Webpublishing-Assistent und der Assistent für die Online druckbestellung verwenden das Übertragungs Manifest, um Details der Datenübertragung zwischen dem Client Computer und dem Serverstandort zu kommunizieren.
ms.assetid: b7bb541c-3bf4-4aab-ac70-c006517e772e
keywords:
- Webpublishing-Assistent, übertragen des Manifests
- Online-druckstellungs-Assistent, übertragen des Manifests
- Übertragungs Manifest
- manifest
- Window. extern, Übertragungs Manifest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fa7b3a35a6f06e2939b6c25f82d12c2b98a7f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858245"
---
# <a name="using-the-transfer-manifest"></a>Verwenden des Übertragungs Manifests

Der Webpublishing-Assistent und der Assistent für die Online druckbestellung verwenden das Übertragungs Manifest, um Details der Datenübertragung zwischen dem Client Computer und dem Serverstandort zu kommunizieren.

## <a name="the-purpose-of-the-transfer-manifest"></a>Der Zweck des Übertragungs Manifests.

Das Übertragungs Manifest beschreibt die an der Übertragung beteiligten Dateien, einschließlich Details wie der Ziel Hierarchie und den Metadaten der Datei. Das Manifest kann durch ein Server seitiges Skript geändert werden, indem ungeeignete Dateien aus der Liste entfernt werden und Informationen darüber hinzugefügt werden, wie und wo die Dateien übertragen werden sollen.

Das Manifest wird als Eigenschaften **Fenster. extern. Property ("transfermanifest")**, ein XML-Dokumentobjektmodell Dokument (DOM) verfügbar gemacht. Weitere Informationen zum XML-DOM finden Sie in der MSDN-Dokumentation zu [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).

Die Organisation der obersten Ebene des Übertragungs Manifests lautet wie folgt:


```
<transfermanifest>
    <filelist/>
    <folderlist/>
    <uploadinfo/>
</transfermanifest>
```



Die serverseitige HTML-Seite kann mithilfe der Knoten im Manifest bestimmte Informationen zu den zu kopierenden Dateien abrufen und dann die Benutzeroberfläche des dienstanders entsprechend ändern. Beispielsweise kann eine Foto Druck Site die Informationen verwenden, um Miniaturansichten der ausgewählten Images anzuzeigen, während ein Speicherort die Informationen verwenden könnte, um sicherzustellen, dass ausreichend Speicherplatz für diesen Benutzer verfügbar ist. Umfassende Informationen zu den Knoten und Attributen für das Übertragen von Manifests finden Sie unter [übertragen des manifest-Schemas](/windows/desktop/shell/interfaces)

Das Schema des Übertragungs Manifests wird als offenes Modell geschrieben, sodass Elemente, die nicht speziell im Schema definiert sind, im Übertragungs Manifest angezeigt werden können. Daher kann eine Anbieter Site proprietäre Elemente zur eigenen Verwendung hinzufügen, ohne die Gültigkeit des Manifests zu beeinträchtigen. Das Schema ist auch so definiert, dass die Reihenfolge der Elemente nicht eingeschränkt ist.

> [!Note]  
> Das Manifest wird jedes Mal neu erstellt, wenn ein neuer Anbieter ausgewählt wird, damit der Anbieter die Möglichkeit hat, Site Informationen im Manifest zu speichern.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schema des Übertragungs Manifests](/windows/desktop/shell/interfaces)
</dt> </dl>

 

 