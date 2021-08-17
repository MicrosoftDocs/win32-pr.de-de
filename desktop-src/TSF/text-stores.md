---
title: Textspeicher
description: Textspeicher
ms.assetid: c827999a-0b74-4e5d-901e-4c2fa1d74929
keywords:
- Textdienstframework (TSF), Textspeicher
- TSF (Textdienstframework),Textspeicher
- TSF-fähige Anwendungen, Textspeicher
- Textspeicher
- Textdienstframework (TSF), Anwendungszeichenposition (ACP)
- TSF (Textdienstframework),Anwendungszeichenposition (ACP)
- TSF-fähige Anwendungen, Anwendungszeichenposition (ACP)
- Anwendungszeichenposition (ACP)
- ACP (Anwendungszeichenposition)
- Textdienstframework (TSF), Anker
- TSF (Textdienstframework),Anchors
- TSF-fähige Anwendungen, Anker
- Anker
- Textdienstframework (TSF), Dokumentsperren
- TSF (Textdienstframework),Dokumentsperren
- TSF-fähige Anwendungen, Dokumentsperren
- Dokumentsperren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89af01edd439dbac23e4dee4b5289101a9bd92ca8180b66b460096b797d32b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950920"
---
# <a name="text-stores"></a>Textspeicher

## <a name="application-character-position-acp"></a>Anwendungszeichenposition (ACP)

Ein ACP ist die Position eines Zeichens oder von Zeichen in einem Textstream, der als Anzahl von Zeichen vom Anfang des Textstreams ausgedrückt wird. Da das ACP-Modell nullbasiert ist, weist das erste Zeichen in einem Textstream den ACP-Wert 0 (null) auf. Beispiel:


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



Ein Textspeicher implementiert ein -Objekt, das die [ITextStoreACP-Schnittstelle](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) unterstützt, wodurch der Textstream in einem ACP ausgedrückt werden kann. Die **ITextStoreACP-Schnittstellenmethoden** verwenden den ACP-Bereich des Textstreams, um den Text zu ändern.

## <a name="anchor-based-applications"></a>Anchor-Based-Anwendungen

Der Manager verwendet die ACP-basierten Methoden nativ, um Text zu bearbeiten. Ein ankerbasierter Ansatz ist jedoch für [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) Clients verfügbar, die [Anker](ranges.md)unterstützen, wobei der Manager [ITextStoreAnchor-](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) und [ITextStoreAnchorSink-Methoden](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) verwendet, um die [ITextStoreACP-](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) und [ITextStoreACPSink-Methoden](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) zu umschließen.

## <a name="document-access-control"></a>Dokument Access Control

Der Textspeicher steuert den Zugriff auf den Textstream mithilfe von [Dokumentsperren.](document-locks.md) Um den Textspeicher zu lesen oder zu ändern, muss der Manager zunächst eine Advise-Senke installieren, die die [ITextStoreACPSink-Schnittstelle](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) unterstützt, indem er die [ITextStoreACP::AdviseSink-Methode aufruft](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) und einen Zeiger auf eine Advise-Senke übergibt. Die Advise-Senke ermöglicht es dem Manager, dokumentsperren für den Textspeicher zu erhalten und Benachrichtigungen zu erhalten, wenn der Textspeicher durch einen anderen Textspeicher als den Manager geändert wird, z. B. Benutzereingaben über die Anwendung. Empfehlungssenken werden weiter unten in diesem Thema erläutert.

## <a name="how-to-initialize-the-text-store"></a>Initialisieren der Text-Store

Eine Anwendung initialisiert einen Textspeicher, indem sie die folgenden Schritte ausschließt:

1.  Erstellen Sie ein Thread-Manager-Objekt basierend auf der [ITfThreadMgr-Schnittstelle,](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) indem Sie die [CoCreateInstance-Funktion](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit einem Zeiger auf ein Thread-Manager-Objekt aufrufen. Im Folgenden wird ein Codebeispiel für die Implementierung eines Thread-Manager-Objekts beschrieben.
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  Aktivieren Sie das Thread-Manager-Objekt, indem Sie die [ITfThreadMgr::Activate-Methode](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) aufrufen. Diese Methode stellt einen Zeiger auf einen [Clientbezeichner](tfclientid.md) bereit, der zum Erstellen eines Kontextobjekts verwendet wird. Der Thread-Manager wird verwendet, um ein Dokument-Manager-Objekt zu implementieren.
3.  Erstellen Sie ein Dokument-Manager-Objekt basierend auf der [ITfDocumentMgr-Schnittstelle,](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) indem Sie die [ITfThreadMgr::CreateDocumentMgr-Methode](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) mit einem Zeiger auf das Dokument-Manager-Objekt aufrufen. Das Dokument-Manager-Objekt wird verwendet, um ein Kontextobjekt zu implementieren, das der Textspeicher ist.
4.  Erstellen Sie ein Kontextobjekt aus dem Dokument-Manager, indem Sie die [ITfDocumentMgr::CreateContext-Methode](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) mit dem Zeiger auf das Textspeicherobjekt und einem Zeiger auf den Clientbezeichner aufrufen, der den Thread-Manager aktiviert. Im Folgenden wird ein Beispiel für das Erstellen eines Kontextobjekts beschrieben:
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  Pushen Sie das Kontextobjekt mit der [ITfDocumentMgr::P ush-Methode](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) auf den Stapel. Es folgt ein Beispiel für das Pushen des Kontextobjekts auf den Stapel:
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a>Ändern der Text-Store

Die **ITfDocumentMgr::P ush-Methode** ruft **ITextStoreACP::AdviseSink** mit einem Zeiger auf die Advise-Senkenschnittstelle auf, um eine neue Advise-Senke zu installieren oder eine vorhandene Advise-Senke zu ändern. Die Advise-Senke empfängt Benachrichtigungen, wenn der Textspeicher durch einen anderen Textspeicher als den Manager geändert wird, z. B. Benutzereingaben für die Anwendung. Anwendungen müssen die [ITfThreadMgrEventSink::OnSetFocus-Methode](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) aufrufen, wenn die Eingabemethode den Fokus erhält. Andere Benachrichtigungen an den Thread-Manager werden durch Aufrufen der entsprechenden **ITextStoreACPSink-Schnittstellenmethoden** bereitgestellt.

Anwendungen sollten die **ITextStoreACPSink-Schnittstellenmethoden** jedoch nicht als Reaktion auf **ITextStoreACP-Schnittstellenmethoden** aufrufen. Anwendungen sollten nur **ITextStoreACPSink-Schnittstellenmethoden** aufrufen, wenn der Textspeicher durch einen anderen Als den Manager geändert wird.

Der Inhalt des Textspeichers kann mit einem temporären Eingabezustand geändert werden, der als [Komposition](compositions.md)bezeichnet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anchors](ranges.md)
</dt> <dt>

[Kompositionen](compositions.md)
</dt> <dt>

[Dokumentsperren](document-locks.md)
</dt> <dt>

[ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)
</dt> <dt>

[Itextstoreacp](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)
</dt> <dt>

[ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)
</dt> <dt>

[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[ITfThreadMgrEventSink::OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus)
</dt> <dt>

[TfClientId](tfclientid.md)
</dt> <dt>

[Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md)
</dt> </dl>

 

 