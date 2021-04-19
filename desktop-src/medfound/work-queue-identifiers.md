---
description: Die folgenden Konstanten identifizieren die Standard-Media Foundation Arbeits Warteschlangen.
ms.assetid: c769f876-83ca-4b04-a054-22fa7146310e
title: Arbeitswarteschlangen-IDs (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecff594bad2a4595862f0bc6457644f86949d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106367980"
---
# <a name="work-queue-identifiers"></a>Bezeichner der Arbeits Warteschlange

Die folgenden Konstanten identifizieren die Standard-Media Foundation Arbeits Warteschlangen.

Anwendungen sollten die mfasync- \_ Rückruf \_ Warteschlange \_ Multithreaded verwenden oder eine Arbeits Warteschlange verwenden, die von [**mflocksharedworkqueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) abgerufen wird, wenn Sie die Ausführungs Priorität steuern möchten. Beachten Sie, dass sich die Standard Prioritäten der Plattform für die Arbeits Warteschlange dynamisch ändern können, wenn eine Anwendung [**registerplatformwithmmcss**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss)aufruft. Weitere Informationen zu Arbeits Warteschlangen finden Sie unter [Arbeits Warteschlangen](work-queues.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante/Wert</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_STANDARD"></span><span id="mfasync_callback_queue_standard"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </dl></td>
<td style="text-align: left;">In den meisten Fällen sollten Anwendungen <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>verwenden.<br/> Diese Arbeits Warteschlange wird für synchrone Vorgänge verwendet. Die Verwendung der Standard Arbeits Warteschlange kann das Risiko eines Deadlocks darstellen. Anwendungen können eine private synchrone Warteschlange oberhalb der multithreadwarteschlange erstellen, indem Sie <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MF belegereserialworkqueue</strong></a>verwenden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_RT"></span><span id="mfasync_callback_queue_rt"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </dl></td>
<td style="text-align: left;">Nicht für allgemeine Anwendungs Verwendung.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_IO"></span><span id="mfasync_callback_queue_io"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </dl></td>
<td style="text-align: left;">Nicht für allgemeine Anwendungs Verwendung.<br/> Diese Arbeits Warteschlange wird intern für e/a-Vorgänge wie das Lesen von Dateien und das Lesen aus dem Netzwerk verwendet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_TIMER"></span><span id="mfasync_callback_queue_timer"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </dl></td>
<td style="text-align: left;">Nicht für allgemeine Anwendungs Verwendung.<br/> Diese Arbeits Warteschlange wird für regelmäßige Rückrufe und geplante Arbeitselemente verwendet. Die folgenden Funktionen stellen Arbeitsaufgaben in diese Warteschlange:<br/>
<ul>
<li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>Mfaddperiodiccallback</strong></a></li>
<li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MF scheduleworkitem</strong></a></li>
<li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MF scheduleworkitemex</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_MULTITHREADED"></span><span id="mfasync_callback_queue_multithreaded"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005 bei der</dt> </dl></td>
<td style="text-align: left;">Diese Multithread-Arbeits Warteschlange sollte in den meisten Fällen verwendet werden. <br/> Diese Arbeits Warteschlange wird für asynchrone Vorgänge in Media Foundation verwendet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION"></span><span id="mfasync_callback_queue_long_function"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </dl></td>
<td style="text-align: left;">Nicht für allgemeine Anwendungs Verwendung. Anwendungen sollten stattdessen <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>verwenden.<br/></td>
</tr>
</tbody>
</table>



Außerdem werden die folgenden Konstanten in Verbindung mit Arbeits Warteschlangen verwendet.



| Konstante/Wert                                                                                                                                                                                                                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASYNC_CALLBACK_QUEUE_UNDEFINED"></span><span id="mfasync_callback_queue_undefined"></span><dl> <dt>**Mfasync \_ Rückruf \_ Warteschlange nicht \_ definiert**</dt> <dt>0x00000000</dt> </dl>           | Nicht definierte Arbeits Warteschlange.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK"></span><span id="mfasync_callback_queue_private_mask"></span><dl> <dt>**Mfasync \_ \_ \_ Private \_ Maske der Rückruf Warteschlange**</dt> <dt>0xFFFF0000</dt> </dl> | Bitmaske zur Unterscheidung von Platt Form Arbeitswarteschlangen von den durch Aufrufen von [**mfbelegcateworkqueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)erstellten.<br/> Für eine Arbeits Warteschlange, die von [**MF belegcateworkqueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)erstellt wurde, ist der folgende Wert ungleich 0 (null):<br/> `(identifier & MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK)`<br/> |
| <span id="MFASYNC_CALLBACK_QUEUE_ALL"></span><span id="mfasync_callback_queue_all"></span><dl> <dt>**Mfasync \_ Rückruf \_ Warteschlange \_ alle**</dt> <dt>0xFFFFFFFF</dt> </dl>                             | Alle Platt Form Arbeitswarteschlangen.<br/>                                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Konstanten](media-foundation-constants.md)
</dt> <dt>

[Arbeits Warteschlangen](work-queues.md)
</dt> <dt>

[Arbeits Warteschlangen und Threading](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 




