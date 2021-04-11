---
title: Dokument Sperren
description: Dokument Sperren
ms.assetid: 3c623c44-b0d3-4b03-8de9-25f1062b5726
keywords:
- Text Dienst Framework (TSF), Dokument Sperren
- TSF (Text Dienst Framework), Dokument Sperren
- TSF-aktivierte Anwendungen, Dokument Sperren
- Dokument Sperren
- Text Services-Framework (TSF), Zeichen Position der Anwendung (ACP)
- TSF (Text Dienst Framework), Zeichen Position der Anwendung (ACP)
- TSF-aktivierte Anwendungen, Anwendungs Zeichen Position (ACP)
- Zeichen Position der Anwendung (ACP)
- ACP (Position des Anwendungs Zeichens)
- Text Dienst Framework (TSF), Anker
- TSF (Text Dienst Framework), Anker
- TSF-aktivierte Anwendungen, Anker
- Anker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438e22d7c77a45d798dfd6d5d7c43eaafa3e09c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206513"
---
# <a name="document-locks"></a>Dokument Sperren

## <a name="the-document-lock-protocol"></a>Das Dokument Sperrprotokoll

Um eine Dokument Sperre für ACP-basierte Anwendungen anzufordern, ruft der TSF-Manager [ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)auf. Bei Anker basierten Anwendungen ruft der TSF-Manager [itextstoreanchor:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)auf. Die Anwendung gewährt die Dokument Sperre durch Aufrufen von [ITextStoreACPSink:: onlockgewährten](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (ACP-basierte Anwendungen) oder [itextstoreanchorsink:: onlockgewährten](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (Anker basierte Anwendungen) in **RequestLock**. Die Sperre ist nur während des **onlockgewährten** -Aufrufes zulässig. Wenn **onlockgewährte** zurückgibt, gilt das Dokument als entsperrt.

## <a name="types-of-document-locks"></a>Typen von Dokument Sperren

Es gibt zwei Arten von Dokument Sperren: schreibgeschützt und Lese-/Schreibzugriff. Eine schreibgeschützte Sperre ermöglicht dem Manager, den Text zu lesen, kann aber keinen Text ändern oder einfügen. Eine Lese-/Schreibsperre ermöglicht dem Manager das Lesen, ändern und Einfügen von Text. Eine schreibgeschützte Sperre wird angefordert, indem TS \_ LF- \_ Lesevorgänge in *dwFlags* angegeben werden. Eine Lese-/Schreibsperre wird angefordert, indem TS LF-Lese \_ \_ Vorgang in *dwFlags* angegeben wird.

## <a name="asynchronous-and-synchronous-requests"></a>Asynchrone und synchrone Anforderungen

Eine Sperranforderung kann entweder synchron oder asynchron sein. Der Manager fordert eine synchrone Sperre mit dem TS \_ LF- \_ synchronisierungsflag in *dwFlags* an. Wenn dieses Flag nicht vorhanden ist, ist die Anforderung asynchron.

## <a name="granting-the-lock"></a>Erteilen der Sperre

Wenn **RequestLock** aufgerufen wird, muss die Anwendung ermitteln, ob das Dokument zurzeit gesperrt ist. Wenn das Dokument nicht gesperrt ist und kein anderer Grund zum Verweigern der Sperre vorhanden ist, sollte die Anwendung *phrSession* auf OK festlegen \_ und s OK zurückgeben \_ .

Wenn das Dokument gesperrt ist und die Sperranforderung synchron ist, sollte die Anwendung *phrSession* auf "TS \_ E \_ synchron" festlegen und "S OK" zurückgeben \_ . Dies weist darauf hin, dass eine synchrone Anforderung nicht erteilt werden kann.

Wenn das Dokument gesperrt ist und die Sperranforderung asynchron ist, sollte die Anwendung die Anforderung in die Warteschlange stellen, *phrSession* auf "TS \_ S \_ Async" festlegen und "S OK" zurückgeben \_ . Wenn das Dokument verfügbar wird, sollte die Anwendung die Anforderung aus der Warteschlange entfernen und **onlockgewährte** abrufen. Diese Warteschlange von Sperr Anforderungen ist optional. Es gibt ein Szenario, das von einer Anwendung unterstützt werden muss. Wenn das Dokument über eine schreibgeschützte Sperre verfügt, lautet die neue Sperranforderung Lese-/Schreibzugriff, und die Anforderung ist asynchron, die Anwendung wurde in **onlockgewährten** aufgerufen, was zu einem Wiedereinstiegs Aufruf von **RequestLock** geführt hat. Die Anwendung sollte *phrSession* auf "TS \_ S \_ Async" festlegen und "S OK" zurückgeben \_ . Nachdem der Aufruf von **onlockgewährte zurückgegeben** wurde, sollte die Anwendung die upgradeanforderung verarbeiten, indem Sie **onlockgewährten** erneut mit "TS LF-Lesevorgang" aufruft \_ \_ .

## <a name="lock-enforcement"></a>Sperr Erzwingung

Die Anwendung muss sicherstellen, dass der richtige Sperrentyp vorhanden ist, bevor der Zugriff auf das Dokument zugelassen wird. Die Anwendung sollte z. b. überprüfen, ob ein Dokument mindestens eine schreibgeschützte Sperre aufweist, bevor das Fortsetzen von [ITextStoreACP:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) oder [itextstoreanchor:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) zugelassen wird. Wenn die richtige Sperre nicht vorhanden ist, sollte die Anwendung TF \_ E \_ NOLOCK zurückgeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Text Speicher](text-stores.md)
</dt> <dt>

[ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[ITextStoreACPSink:: onlockgewährten](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[ITextStoreACP:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext)
</dt> <dt>

[Itextstoreanchor:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[Itextstoreanchorsink:: onlockgewährten](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> <dt>

[Itextstoreanchor:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext)
</dt> </dl>

 

 




