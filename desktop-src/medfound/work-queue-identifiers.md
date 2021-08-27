---
description: Die folgenden Konstanten identifizieren die Media Foundation Arbeitswarteschlangen.
ms.assetid: c769f876-83ca-4b04-a054-22fa7146310e
title: Arbeitswarteschlangenbezeichner (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d454e8b2a199a9c132bf6ea287f31d7d3e5102
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470227"
---
# <a name="work-queue-identifiers"></a>Arbeitswarteschlangenbezeichner

Die folgenden Konstanten identifizieren die Media Foundation Arbeitswarteschlangen.

Anwendungen sollten MFASYNC CALLBACK QUEUE MULTITHREADED oder eine Arbeitswarteschlange verwenden, die von \_ \_ \_ [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) erhalten wurde, wenn sie die Ausführungspriorität steuern möchten. Beachten Sie, dass sich die Standardprioritäten der Plattformarbeitswarteschlange dynamisch ändern können, wenn eine Anwendung [**RegisterPlatformWithMMCSS aufruft.**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss) Weitere Informationen zu Arbeitswarteschlangen finden Sie unter [Arbeitswarteschlangen](work-queues.md).




| Konstante/Wert | BESCHREIBUNG | 
|----------------|-------------|
| <span id="MFASYNC_CALLBACK_QUEUE_STANDARD"></span><span id="mfasync_callback_queue_standard"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt><dt>0x00000001</dt></dl> | In den meisten Fällen sollten Anwendungen <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED.</strong><br /> Diese Arbeitswarteschlange wird für synchrone Vorgänge verwendet. Die Verwendung der Standardarbeitswarteschlange kann das Risiko eines Deadlocks darstellen. Anwendungen können mithilfe von <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>eine private synchrone Warteschlange über der Multithreadwarteschlange erstellen.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_RT"></span><span id="mfasync_callback_queue_rt"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt><dt>0x00000002</dt></dl> | Nicht zur allgemeinen Anwendungsnutzung.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_IO"></span><span id="mfasync_callback_queue_io"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt><dt>0x00000003</dt></dl> | Nicht zur allgemeinen Anwendungsnutzung.<br /> Diese Arbeitswarteschlange wird intern für E/A-Vorgänge wie das Lesen von Dateien und das Lesen aus dem Netzwerk verwendet.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_TIMER"></span><span id="mfasync_callback_queue_timer"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt><dt>0x00000004</dt></dl> | Nicht zur allgemeinen Anwendungsnutzung.<br /> Diese Arbeitswarteschlange wird für regelmäßige Rückrufe und geplante Arbeitselemente verwendet. Die folgenden Funktionen setzen Arbeitselemente in diese Warteschlange:<br /><ul><li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></li><li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></li><li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></li></ul> | 
| <span id="MFASYNC_CALLBACK_QUEUE_MULTITHREADED"></span><span id="mfasync_callback_queue_multithreaded"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt><dt>0x00000005</dt></dl> | Diese Multithreadarbeitswarteschlange sollte in den meisten Fällen verwendet werden. <br /> Diese Arbeitswarteschlange wird für asynchrone Vorgänge im gesamten Media Foundation.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION"></span><span id="mfasync_callback_queue_long_function"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt><dt>0x00000007</dt></dl> | Nicht zur allgemeinen Anwendungsnutzung. Anwendungen sollten stattdessen <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED.</strong><br /> | 




Darüber hinaus werden die folgenden Konstanten in Verbindung mit Arbeitswarteschlangen verwendet.



| Konstante/Wert                                                                                                                                                                                                                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASYNC_CALLBACK_QUEUE_UNDEFINED"></span><span id="mfasync_callback_queue_undefined"></span><dl> <dt>**MFASYNC \_ RÜCKRUFWARTESCHLANGE \_ \_ UNDEFINED-0X00000000**</dt> <dt></dt> </dl>           | Nicht definierte Arbeitswarteschlange.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK"></span><span id="mfasync_callback_queue_private_mask"></span><dl> <dt>**MFASYNC \_ CALLBACK \_ QUEUE \_ PRIVATE \_ MASK-0xFFFF0000**</dt> <dt></dt> </dl> | Bitmaske, um Plattformarbeitswarteschlangen von denen zu unterscheiden, die durch Aufrufen von [**MFAllocateWorkQueue erstellt wurden.**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)<br/> Für eine arbeitswarteschlange, die von [**MFAllocateWorkQueue erstellt**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)wurde, ist der folgende Wert ungleich null:<br/> `(identifier & MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK)`<br/> |
| <span id="MFASYNC_CALLBACK_QUEUE_ALL"></span><span id="mfasync_callback_queue_all"></span><dl> <dt>**MFASYNC \_ CALLBACK \_ QUEUE \_ ALL**</dt> <dt>0xFFFFFFFF</dt> </dl>                             | Alle Plattformarbeitswarteschlangen.<br/>                                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Konstanten](media-foundation-constants.md)
</dt> <dt>

[Arbeitswarteschlangen](work-queues.md)
</dt> <dt>

[Verbesserungen bei Arbeitswarteschlangen und Threading](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 




