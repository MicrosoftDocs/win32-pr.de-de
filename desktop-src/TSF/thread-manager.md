---
title: Thread-Manager
description: Der Thread-Manager ist die Basiskomponente des TSF-Managers.
ms.assetid: fd43b4c3-80bb-4118-a880-bdea07022c95
keywords:
- Text Services-Framework (TSF), Thread-Manager
- TSF (Text Dienst Framework), Thread-Manager
- Text Dienste, Thread-Manager
- TSF-aktivierte Anwendungen, Thread-Manager
- Thread-Manager
- TSF-Manager
- Ereignisbenachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b29596c5c39267181c6a2c301aede3f15ca7297
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039237"
---
# <a name="thread-manager"></a>Thread-Manager

Der Thread-Manager ist die Basiskomponente des TSF-Managers. Der Thread-Manager führt häufige Aufgaben aus, die sich auf Anwendungen und Text Dienste (Clients) beziehen. Zu diesen Tasks gehören u. a. die Aktivierung und Deaktivierung von TSF-Text Diensten, die Erstellung von Dokument-Managern und die Wartung der ordnungsgemäßen Beziehung zwischen Dokumenten und dem Eingabefokus. Der Thread-Manager wird von der [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) -Schnittstelle definiert.

Die meisten Schnittstellen und Objekte, die vom TSF-Manager bereitgestellt werden, können mithilfe der Methoden abgerufen werden, die die Thread-Manager-Schnittstelle bereitstellt.

## <a name="applications"></a>Anwendungen

Eine Anwendung erstellt ein Thread-Manager-Objekt durch Aufrufen von [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit CLSID \_ tfthreadmgr.

## <a name="text-services"></a>Text Dienste

Ein Text Dienst erhält ein Thread-Manager-Objekt in der [itftextinputprocessor:: Aktivierungs](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) -Methode von Text Service.

## <a name="event-notifications"></a>Ereignisbenachrichtigungen

Der Thread-Manager stellt auch Ereignis Benachrichtigungen für Clients bereit. In TSF werden Ereignis Benachrichtigungen mithilfe einer Ereignis Senke bereitgestellt, bei der es sich um ein COM-Objekt handelt. Zum Empfangen von Benachrichtigungen vom Thread-Manager implementiert ein Client ein [itfthreadmgreventsink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) -Objekt und installiert die Ereignis Senke. Die Ereignis Senke wird installiert, indem der Thread-Manager nach IID \_ itfsource abgefragt und [itfsource:: AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) mit IID \_ itfthreadmgreventsink aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[ITF textinputprocessor:: Aktivierung](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[Itfthreadmgreventsink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink)
</dt> <dt>

[ITF Source:: AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> </dl>

 

 