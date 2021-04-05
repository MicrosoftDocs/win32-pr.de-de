---
title: Verwenden von benutzerdefinierten senken
description: Verwenden von benutzerdefinierten senken
ms.assetid: 7151583a-c7ab-40b0-a7bf-ddd56f93b7aa
keywords:
- Advanced Systems Format (ASF), benutzerdefinierte senken
- ASF (Advanced Systems Format), Custom Sinks
- Advanced Systems Format (ASF), senken
- ASF (Advanced Systems Format), senken
- senken, benutzerdefinierte senken
- benutzerdefinierte senken, Informationen zu
- Writer-senken, benutzerdefinierte senken
- benutzerdefinierte senken, iwmschreitersink-Schnittstelle
- Iwmschreibsink
- Writer-senken, iwmschreitersink-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e324d654fa8c85d6145b0f4bf8f20de1f06e125f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723480"
---
# <a name="using-custom-sinks"></a>Verwenden von benutzerdefinierten senken

Wenn Sie einen speziellen Schreib Bedarf haben, können Sie eigene Writer-senken erstellen. Der Writer verwaltet die unidirektionale Kommunikation mit einer Senke, indem er die Methoden von [**iwmschreitersink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)aufruft. Um eine eigene Senke zu erstellen, implementieren Sie die **iwmschreitersink** -Schnittstelle in einer Klasse in Ihrer Anwendung. Dieser Prozess ähnelt dem Implementieren anderer Rückruf Schnittstellen, die von den Objekten des Windows Media Format SDK verwendet werden. Weitere Informationen über Rückrufe finden Sie unter [Verwenden der Rückruf Methoden](using-the-callback-methods.md).

Der in [**iwmwrite:: onheader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) empfangene Puffer sollte an den Anfang der Datei geschrieben werden, und alle in [**ondataunit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) empfangenen Puffer sollten sequenziell ausgeschrieben werden. **Onheader** wird zu Beginn aufgerufen, kann aber auch zu anderen Zeiten aufgerufen werden. wenn dies der Fall ist, sollten Sie, wenn möglich, den ursprünglichen Header überschreiben. Wenn die Anwendung aus irgendeinem Grund nicht in der Lage ist, sollten Sie die nachfolgenden **onheader** -Aufrufe einfach ignorieren.

Die benutzerdefinierte Senke sollte ihren Status an Ihre Schreib Anwendung übermitteln, indem Sie Aufrufe an die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Rückruf Methode sendet. Wenn Sie die Senke als COM-Objekt implementieren, möchten Sie möglicherweise die [**iwmregistercallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) -Schnittstelle verfügbar machen. Sie können jedoch die Adresse des **OnStatus** -Rückrufs an die Senke übergeben und in beliebiger Weise einen Kontext festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Writer-senken**](working-with-writer-sinks.md)
</dt> </dl>

 

 




