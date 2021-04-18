---
description: Das frei Hand Blog Beispiel veranschaulicht verschiedene nützliche Verfahren, die in frei Hand fähigen Webanwendungen verwendet werden können.
ms.assetid: 4a5a453d-e3c1-40e6-b0eb-99009f0024dd
title: Webanwendungen Ink-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b14e368c1d2e97e35afa6d72a0fe082f304c5fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343671"
---
# <a name="ink-enabled-web-applications"></a>Webanwendungen Ink-Enabled

Das frei Hand [Blog](ink-blog-web-sample.md) Beispiel veranschaulicht verschiedene nützliche Verfahren, die in frei Hand fähigen Webanwendungen verwendet werden können. Hierzu gehören: testen, ob der Client Computer frei Hand fähige Steuerelemente unterstützen kann, frei Hand Daten an einen Server übermittelt und frei Hand Daten auf einer Webseite anzeigt.

## <a name="testing-ink-enablement"></a>Testen der frei Hand Aktivierung

Es kann nützlich sein, zu testen, ob der Client Computer frei Hand fähige Steuerelemente anzeigen kann. Dies ermöglicht es Ihnen, die webpageshow ein Steuerelement anzuzeigen, wenn es sich bei dem Client um einen Tablet PC oder einen anderen handelt, wenn dies nicht der Fall ist. Eine Möglichkeit, dies zu testen, besteht darin, ein Objekt zu erstellen, z. b. ein [InkOverlay](/previous-versions/ms833057(v=msdn.10))-Objekt, das nur auf einem Computer erstellt werden kann, auf dem das Betriebssystem Windows Vista, das Windows XP Tablet PC Edition oder das Windows XP Tablet PC Edition SDK (Software Development Kit) installiert ist. Wenn Sie das Objekt in einem try/catch-Block erstellen und alle ausgelösten Ausnahmen abfangen (häufig wird eine file- [FoundException](/previous-versions/windows/) ausgelöst, um anzugeben, dass die Assembly mit diesem Steuerelement nicht gefunden werden kann), können Sie erkennen, ob der Client Computer frei Hand Steuerelemente unterstützen kann. Im Beispiel befindet sich dieser Code im Konstruktor der- `InkArea` Klasse.

## <a name="submitting-ink-data"></a>Senden von frei Hand Daten

Eine einfache Möglichkeit, Daten zu übermitteln, besteht darin, die Daten aus dem Freihand-aktivierten Steuerelement zu übertragen, in ein ausgeblendetes Formular zu übertragen und dann das Formular Die frei Hand Eingaben können mithilfe der [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) -Methode serialisiert und anschließend in eine Zeichenfolge konvertiert werden. Im Beispiel wird das ausgeblendete Formular in "addblog. aspx" definiert, und die Freihand-Serialisierung wird in behandelt `InkArea.SerializeInkData` , wobei die frei Hand Eingaben in ein GIF-Bild serialisiert werden. (Beachten Sie, dass es auch in anderen Formaten, wie z. b. ISF (Ink serialisiert Format), serialisiert werden kann.

## <a name="displaying-ink-data"></a>Anzeigen von frei Hand Daten

Im Beispiel verfügt addblog. aspx. cs über eine Methode mit `Page_Load` dem Namen, die die Daten abruft, die an den Server gesendet und in Dateien gespeichert werden. Anschließend werden auf dem Server, der IMG-Tags enthält, die auf die Dateien mit den GIF-Bildern verweisen, Webseiten generiert. Jetzt müssen Sie nur zu diesen Seiten navigieren, um Bilder der frei Hand Eingabe anzuzeigen. (Beachten Sie Folgendes: Wenn Sie die frei Hand Eingabe in ein anderes Format serialisiert hätten (z. b. "Ink serialisiert Format", ISF), müssten Sie die frei Hand Eingaben in ein Bild auf dem Server konvertieren, um Sie auf Clients anzuzeigen, bei denen es sich nicht um Tablets handelt.)

Tablet PC-Clients können die frei Hand Eingaben in ein frei Hand fähiges Steuerelement laden und es dem Benutzer ermöglichen, die frei Hand Eingaben mithilfe von ISF zu bearbeiten. Dies gilt auch für frei Hand Eingaben, die mithilfe des **GIF** -Werts der [PersistenceFormat](/previous-versions/ms827245(v=msdn.10)) -Enumeration gespeichert werden, da die ISF-Daten in den GIF-Metadaten enthalten sind.

 

 
