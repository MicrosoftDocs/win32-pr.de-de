---
description: Im Ink-Blogbeispiel werden verschiedene nützliche Techniken veranschaulicht, die in Ink-fähigen Webanwendungen verwendet werden können.
ms.assetid: 4a5a453d-e3c1-40e6-b0eb-99009f0024dd
title: Ink-Enabled Webanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8097bd55c34abbcb4469d74642e9dbc9a5f29e3b0b7110a76543fd40f5b1ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118043491"
---
# <a name="ink-enabled-web-applications"></a>Ink-Enabled Webanwendungen

Im [Ink-Blogbeispiel](ink-blog-web-sample.md) werden verschiedene nützliche Techniken veranschaulicht, die in Ink-fähigen Webanwendungen verwendet werden können. Dazu gehören: Testen, ob der Clientcomputer Freihandsteuerelemente unterstützen kann, Übermitteln von Freihanddaten an einen Server und Anzeigen von Freihanddaten auf einer Webseite.

## <a name="testing-ink-enablement"></a>Testen der Aktivierung von Ink

Es kann hilfreich sein, zu testen, ob auf dem Clientcomputer Steuerelemente mit Ink-Aktivierung angezeigt werden können. Dadurch können Sie festlegen, dass das Steuerelementwebpage ein Steuerelement zeigt, wenn es sich bei dem Client um einen Tablet-PC handelt, oder um ein anderes Steuerelement, wenn dies nicht dere ist. Eine Möglichkeit, dies zu testen, besteht darin, ein Objekt wie z.B. [inkOverlay](/previous-versions/ms833057(v=msdn.10))zu erstellen, das nur auf einem Computer erstellt werden kann, auf dem das Windows Vista, Windows Betriebssystem XP Tablet PC Edition oder das Windows XP Tablet PC Edition Software Development Kit (SDK) installiert ist. Wenn Sie das Objekt in einem try/catch-Block erstellen und alle ausgelösten Ausnahmen abfangen (häufig wird eine [FileNotFoundException](/previous-versions/windows/) ausgelöst, um anzugeben, dass die Assembly mit diesem Steuerelement nicht gefunden werden kann), können Sie erkennen, ob der Clientcomputer Freihandsteuerelemente unterstützen kann. Im Beispiel finden Sie diesen Code im Konstruktor der `InkArea` -Klasse.

## <a name="submitting-ink-data"></a>Übermitteln von Ink-Daten

Eine einfache Möglichkeit zum Übermitteln von Daten besteht darin, die Daten aus Ihrem Freihandsteuerelement zu übernehmen, in ein ausgeblendetes Formular zu übertragen und dann das Formular zu übermitteln. Die Ink-Datei kann mithilfe der [Save-Methode](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) serialisiert und dann in eine Zeichenfolge konvertiert werden. Im Beispiel wird das ausgeblendete Formular in AddBlog.aspx definiert, und die Ink-Serialisierung wird in `InkArea.SerializeInkData` behandelt, wobei die Ink-Datei in ein GIF-Bild serialisiert wird. (Beachten Sie, dass die Serialisierung auch in anderen Formaten ähnlich sein kann, z. B. im serialisierten Ink-Format (ISF).)

## <a name="displaying-ink-data"></a>Anzeigen von Ink-Daten

Im Beispiel verfügt AddBlog.aspx.cs über eine Methode namens `Page_Load` , die die Daten abruft, die an den Server gesendet werden, und diese in Dateien speichert. Anschließend werden Webseiten auf dem Server generiert, die Img-Tags enthalten, die auf die Dateien mit den GIF-Bildern verweisen. Jetzt müssen Sie nur zu diesen Seiten navigieren, um Bilder der Ink anzuzeigen. (Beachten Sie Folgendes: Wenn Sie die Ink-Datei mit einem anderen Format serialisiert hätten, z. B. serialisiertes Freihandformat (ISF), müssten Sie die Ink-Datei in ein Bild auf dem Server konvertieren, um sie auf Clients anzuzeigen, die keine Tablets sind.)

Tablet PC-Clients können die Ink-Datei wieder in ein Steuerelement laden, das für Die-Ink-Unterstützung aktiviert ist, und es dem Benutzer ermöglichen, die Ink-Datei mithilfe von ISF zu bearbeiten. Dies gilt auch für Ink-Dateien, die mit dem **GIF-Wert** der [PersistenceFormat-Enumeration](/previous-versions/ms827245(v=msdn.10)) gespeichert werden, da die ISF-Daten in den GIF-Metadaten enthalten sind.

 

 
