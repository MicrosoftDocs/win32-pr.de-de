---
description: TSPIMessage ist ein Enumerationstyp, der den Satz zusätzlicher LINEEVENT- und PHONEEVENT-Funktionen definiert, die in TSPI angezeigt werden und nicht in TAPI angezeigt werden.
ms.assetid: b3c4ce68-033f-42f1-8c37-66326d21bf32
title: TSPIMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f74b412d131fc40a13f9da13dc86ba4f31a3becf6bb747e95131bc3bb0e2bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739160"
---
# <a name="tspimessage"></a>TSPIMessage

**TSPIMessage** ist ein Enumerationstyp, der den Satz zusätzlicher [**LINEEVENT-**](/windows/win32/api/tspi/nc-tspi-lineevent) und [**PHONEEVENT-Funktionen**](/windows/desktop/api/tspi/nc-tspi-phoneevent) definiert, die in TSPI angezeigt werden und nicht in TAPI angezeigt werden.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>\_TSPI-NACHRICHTENBASIS \_
</dt> <dd>

Die niedrigste Zahl im Bereich tspi-spezifischer Nachrichtenwerte. Dieser Wert allein hat keine Bedeutung, dient aber als Grundlage für die Definition der anderen Werte.

</dd> <dt>

<span id="LINE_NEWCALL"></span><span id="line_newcall"></span>LINE \_ NEWCALL
</dt> <dd>

Gibt an, dass ein neuer, eingehender Anruf eingetroffen ist, und führt ihn in TAPI ein. Dies muss die erste Nachricht sein, die für einen neuen eingehenden Anruf an TAPI gesendet wird. TAPI gibt seinen nicht transparenten Bezeichner für den Aufruf als Teil der Behandlung dieser Nachricht zurück.

</dd> <dt>

<span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>LINE \_ CALLDEVSPECIFIC
</dt> <dd>

Gibt an, dass ein gerätespezifisches Ereignis auf einem Anrufgerät aufgetreten ist.

</dd> <dt>

<span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>LINE \_ CALLDEVSPECIFICFEATURE
</dt> <dd>

Gibt an, dass ein gerätespezifisches Featureereignis auf einem Anrufgerät aufgetreten ist.

</dd> </dl>

 

 
