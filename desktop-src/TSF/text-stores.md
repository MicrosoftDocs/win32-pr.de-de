---
title: Text Speicher
description: Text Speicher
ms.assetid: c827999a-0b74-4e5d-901e-4c2fa1d74929
keywords:
- Text Dienst Framework (TSF), Text Speicher
- TSF (Text Dienst Framework), Text Speicher
- TSF-aktivierte Anwendungen, Text Speicher
- Text Speicher
- Text Services-Framework (TSF), Zeichen Position der Anwendung (ACP)
- TSF (Text Dienst Framework), Zeichen Position der Anwendung (ACP)
- TSF-aktivierte Anwendungen, Anwendungs Zeichen Position (ACP)
- Zeichen Position der Anwendung (ACP)
- ACP (Position des Anwendungs Zeichens)
- Text Dienst Framework (TSF), Anker
- TSF (Text Dienst Framework), Anker
- TSF-aktivierte Anwendungen, Anker
- Anker
- Text Dienst Framework (TSF), Dokument Sperren
- TSF (Text Dienst Framework), Dokument Sperren
- TSF-aktivierte Anwendungen, Dokument Sperren
- Dokument Sperren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1234f71fa799cf911ff7ede89915068f69417a00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039180"
---
# <a name="text-stores"></a>Text Speicher

## <a name="application-character-position-acp"></a>Zeichen Position der Anwendung (ACP)

Eine ACP ist die Position eines Zeichens oder von Zeichen in einem Textstream, der als die Anzahl der Zeichen vom Anfang des Textstreams ausgedrückt wird. Da das ACP-Modell Null basiert, weist das erste Zeichen in einem Textstream eine ACP von 0 (null) auf. Beispiel:


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



Ein Text Speicher implementiert ein Objekt, das die [ITextStoreACP-](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) Schnittstelle unterstützt, wodurch der Textstream in einer ACP ausgedrückt werden kann. Die **ITextStoreACP-** Schnittstellen Methoden verwenden den ACP-Bereich des Textstreams, um den Text zu ändern.

## <a name="anchor-based-applications"></a>Anchor-Based Anwendungen

Der Manager verwendet die ACP-basierten Methoden, um Text zu bearbeiten. Ein Anker basierter Ansatz ist jedoch für [Microsoft-Active Accessibility](../winauto/microsoft-active-accessibility.md) Clients verfügbar, die [Anker](ranges.md)unterstützen, wobei der Manager die itextstoreanchor-Methode und die [itextstoreanchorsink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) -Methode verwendet, um die [ITextStoreACP-](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) Methode und die [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) -Methode zu umschließen. [](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)

## <a name="document-access-control"></a>Dokument Access Control

Der Text Speicher steuert den Zugriff auf den Textstream mithilfe von [Dokument Sperren](document-locks.md). Um den Text Speicher zu lesen oder zu ändern, muss der Manager zuerst eine Benachrichtigungs Senke installieren, die die [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) -Schnittstelle unterstützt, indem Sie die [ITextStoreACP:: AdviseSink-](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) Methode aufrufen und einen Zeiger an eine Benachrichtigungs Senke übergibt. Die Benachrichtigungs Senke ermöglicht dem Manager das Abrufen von Dokument Sperren im Text Speicher und das Empfangen von Benachrichtigungen, wenn der Text Speicher von einem anderen als dem Vorgesetzten geändert wird, z. b. Benutzereingaben durch die Anwendung. Empfehlung-senken werden weiter unten in diesem Thema erläutert.

## <a name="how-to-initialize-the-text-store"></a>Initialisieren des Text Stores

Eine Anwendung initialisiert einen Text Speicher, indem die folgenden Schritte ausgeführt werden:

1.  Erstellen Sie ein Thread-Manager-Objekt auf Grundlage der [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) -Schnittstelle, indem Sie die [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion mit einem Zeiger auf ein Thread-Manager-Objekt aufrufen. Im folgenden finden Sie ein Codebeispiel für die Implementierung eines Thread-Manager-Objekts.
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  Aktivieren Sie das Thread-Manager-Objekt, indem Sie die [ITfThreadMgr:: Aktivierungs](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) -Methode aufrufen. Diese Methode stellt einen Zeiger auf einen [Client Bezeichner](tfclientid.md) bereit, der zum Erstellen eines Kontext Objekts verwendet wird. Der Thread-Manager wird verwendet, um ein Dokument-Manager-Objekt zu implementieren.
3.  Erstellen Sie ein Dokument-Manager-Objekt auf der Grundlage der [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) -Schnittstelle, indem Sie die [ITfThreadMgr:: createdocumentmgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) -Methode mit einem Zeiger auf das Dokument-Manager-Objekt aufrufen. Das Dokument-Manager-Objekt wird verwendet, um ein Kontext Objekt zu implementieren, das der Text Speicher ist.
4.  Erstellen Sie ein Kontext Objekt aus dem Dokument-Manager, indem Sie die [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) -Methode mit dem Zeiger auf das Text Speicher Objekt und einen Zeiger auf den Client Bezeichner aus der Aktivierung des Thread-Managers aufrufen. Im folgenden finden Sie ein Beispiel für die Erstellung eines Kontext Objekts:
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  Verschieben Sie das Kontext Objekt mit der [ITF documentmgr::P USH](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) -Methode auf den Stapel. Im folgenden finden Sie ein Beispiel für das Übertragen des Kontext Objekts auf den Stapel:
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a>Vorgehensweise beim Ändern des Text Stores

Die **ITfDocumentMgr::P USH** -Methode ruft **ITextStoreACP:: AdviseSink** mit einem Zeiger auf die Schnittstelle für die Benachrichtigungs Senke auf, um eine neue Empfehlung-Senke zu installieren oder eine vorhandene Hinweis Senke zu ändern. Die Benachrichtigungs Senke empfängt Benachrichtigungen, wenn der Text Speicher von einem anderen als dem Vorgesetzten geändert wird, z. b. Benutzereingaben für die Anwendung. Anwendungen müssen die [itfthreadmgreventsink:: OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) -Methode aufrufen, wenn die Eingabemethode den Fokus erhält. Andere Benachrichtigungen an den Thread-Manager werden durch Aufrufen der entsprechenden **ITextStoreACPSink** -Schnittstellen Methoden bereitgestellt.

Anwendungen sollten jedoch nicht die Methoden der **ITextStoreACPSink** -Schnittstelle als Reaktion auf **ITextStoreACP-** Schnittstellen Methoden aufzurufen. Anwendungen sollten nur **ITextStoreACPSink** -Schnittstellen Methoden aufzurufen, wenn der Text Speicher von einem anderen als dem Vorgesetzten geändert wird.

Der Inhalt des Text Speicher kann mit einem temporären Eingabe Zustand namens [Komposition](compositions.md)geändert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anchors](ranges.md)
</dt> <dt>

[Ablage](compositions.md)
</dt> <dt>

[Dokument Sperren](document-locks.md)
</dt> <dt>

[ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)
</dt> <dt>

[ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[Itextstoreanchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)
</dt> <dt>

[Itextstoreanchorsink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)
</dt> <dt>

[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[Itfthreadmgreventsink:: OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus)
</dt> <dt>

[Tfclientid](tfclientid.md)
</dt> <dt>

[Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md)
</dt> </dl>

 

 