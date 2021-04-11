---
description: Der Typ der von Ihnen erstellten Anwendung legt fest, welches frei Hand Persistenzformat unterstützt wird
ms.assetid: bd0a4382-f014-4f03-990d-d2f96aa76ab8
title: Auswählen der zu unterstützten Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 891fa1c21dd3178e925deab27525afa7fa70fa22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218379"
---
# <a name="choosing-which-formats-to-support"></a>Auswählen der zu unterstützten Formate

Der Typ der von Ihnen erstellten Anwendung legt fest, welches frei Hand Persistenzformat unterstützt wird

## <a name="single-ink-object-applications"></a>Single Ink Object-Anwendungen

Anwendungen, deren Dokumente nur frei Hand Eingaben enthalten, sollten ISF (Ink serialisiert Format) verwenden. Sie sollten in der Lage sein, das frei Hand Format (Ink Serialized Format) zu kopieren und einzufügen. Ein Beispiel hierfür ist eine Anwendung zum Zeichnen oder Annotation. Diese Anwendungen können die [**ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)-Methode und die [**ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste) -Methode verwenden.

## <a name="complex-applications"></a>Komplexe Anwendungen

Anwendungen, deren Dokumente andere Inhalte enthalten, wie z. b. Text, sollten zusätzlich zu ISF HTML mit den Dateien für die Graphics Interchange Format (GIF) kopieren. Der HTML-Code selbst muss von der Anwendung generiert werden, obwohl die Tablet PC-APIs (Application Programming Interfaces) GIF-Dateien generieren. Diese Anwendungen sollten außerdem in der Lage sein, ISF für die Interoperabilität mit den oben beschriebenen Anwendungen zu kopieren und einzufügen.

## <a name="rtf"></a>RTF

Eine Anwendung sollte in der Lage sein, das Rich-Text-Format (RTF) zu schaffen, wenn die Interoperabilität mit Microsoft Word 2002 oder anderen Legacy Anwendungen erforderlich ist.

## <a name="mime-support"></a>MIME-Unterstützung

In der folgenden Tabelle sind die empfohlenen Multipurpose Internet Mail Extensions (MIME)-Header und Dateierweiterungen für frei Hand Eingaben aufgelistet, die in Dateien mit ISF oder GIF persistent gespeichert werden. Diese Werte befinden sich in der [**PersistenceFormat**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat) -Enumeration.



| Persistenzformat            | MIME-Header                                                                                    | Dateierweiterung            |
|-------------------------------|------------------------------------------------------------------------------------------------|---------------------------|
| **Base64Gif**                 | Inhaltstyp: Application/x-ms-Ink Content-Transfer-Encoding: Base64<br/>                | Nicht verfügbar<br/> |
| **Base64InkSerializedFormat** | Content-Type: Content-Type: Image/GIF; Format = Ink Content-Transfer-Encoding: Base64<br/> | Nicht verfügbar<br/> |
| **GIF**                       | Inhaltstyp: Application/x-ms-Ink<br/>                                                  | .gif<br/>           |
| **InkSerializedFormat**       | Content-Type: Content-Type: Image/GIF; Format = Ink<br/>                                   | . ISF<br/>           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**PersistenceFormat-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat)
</dt> </dl>

 

 




