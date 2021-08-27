---
description: Der Typ der Anwendung, die Sie erstellen, bestimmt, welches Ink-Persistenzformat unterstützt werden soll.
ms.assetid: bd0a4382-f014-4f03-990d-d2f96aa76ab8
title: Auswählen der zu unterstützenden Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b8b2197c37db603388a4191e08114800aaba37ee8e89803c7ddfb08be18d3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111000"
---
# <a name="choosing-which-formats-to-support"></a>Auswählen der zu unterstützenden Formate

Der Typ der Anwendung, die Sie erstellen, bestimmt, welches Ink-Persistenzformat unterstützt werden soll.

## <a name="single-ink-object-applications"></a>Einzel-Ink-Objektanwendungen

Anwendungen, deren Dokumente nur Ink enthalten, sollten das serialisierte Ink-Format (ISF) verwenden. Sie sollten in der Lage sein, Daten zu kopieren und serialisiertes Freihandformat (ISF) einfüge. Ein Beispiel hierfür ist eine Anwendung zum Zeichnen oder Anmerkungen. Diese Anwendungen können die [**Methoden ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)und [**ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste) verwenden.

## <a name="complex-applications"></a>Komplexe Anwendungen

Anwendungen, deren Dokumente andere Inhalte enthalten, z. B. Text, sollten zusätzlich zur ISF HTML mit Graphics Interchange Format (GIF)-Dateien kopieren. Der HTML-Code selbst muss von der Anwendung generiert werden, obwohl die Anwendungsprogrammierschnittstellen (APIs) von Tablet PC GIF-Dateien generieren. Diese Anwendungen sollten auch isf kopieren und einfügen können, um die Interoperabilität mit den oben beschriebenen Anwendungen zu gewährleisten.

## <a name="rtf"></a>RTF

Eine Anwendung sollte in der Lage sein, RTF (Rich Text Format) zu erzeugen, wenn Interoperabilität mit Microsoft Word 2002 oder anderen Legacyanwendungen erforderlich ist.

## <a name="mime-support"></a>MIME-Unterstützung

In der folgenden Tabelle sind die Multipurpose Internet Mail Extensions(MIME)-Header und Dateierweiterungen für Ink aufgeführt, die mithilfe von ISF oder GIF in Dateien beibehalten werden. Diese Werte befinden sich in der [**PersistenceFormat-Enumeration.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat)



| Persistenzformat            | MIME-Header                                                                                    | Dateierweiterung            |
|-------------------------------|------------------------------------------------------------------------------------------------|---------------------------|
| **Base64Gif**                 | Content-Type: application/x-ms-ink Content-Transfer-Encoding: base64<br/>                | Nicht verfügbar<br/> |
| **Base64InkSerializedFormat** | Content-Type: Content-Type: image/gif; format=ink Content-Transfer-Encoding: base64<br/> | Nicht verfügbar<br/> |
| **Gif**                       | Content-Type: application/x-ms-ink<br/>                                                  | .gif<br/>           |
| **InkSerializedFormat**       | Content-Type: Content-Type: image/gif; format=ink<br/>                                   | ISF<br/>           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**PersistenceFormat-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat)
</dt> </dl>

 

 




