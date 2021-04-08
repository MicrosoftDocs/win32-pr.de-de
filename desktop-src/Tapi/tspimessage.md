---
description: Tspimess Age ist ein Enumerationstyp, der den Satz zusätzlicher LineEvent-und phoneevent-Funktionen definiert, die in TSPI angezeigt werden und nicht in TAPI angezeigt werden.
ms.assetid: b3c4ce68-033f-42f1-8c37-66326d21bf32
title: Tspimess Age
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ed5f081c367c675c565f64146b2201890b8306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753720"
---
# <a name="tspimessage"></a>Tspimess Age

**Tspimess Age** ist ein Enumerationstyp, der den Satz zusätzlicher [**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent) -und [**phoneevent**](/windows/desktop/api/tspi/nc-tspi-phoneevent) -Funktionen definiert, die in TSPI angezeigt werden und nicht in TAPI angezeigt werden.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>TSPI- \_ Nachrichten \_ Basis
</dt> <dd>

Die niedrigste Zahl im Bereich von TSPI-spezifischen Nachrichten Werten. Dieser Wert hat keine Bedeutung, sondern dient als Basis zum Definieren der anderen Werte.

</dd> <dt>

<span id="LINE_NEWCALL"></span><span id="line_newcall"></span>Zeilen \_ neueinrufe
</dt> <dd>

Gibt an, dass ein neuer, eingehender-Aufrufvorgang eingetroffen ist und ihn in TAPI einführt. Dies muss die erste Nachricht sein, die für einen neuen eingehenden-Befehl an TAPI gesendet wird. TAPI gibt seinen nicht transparenten Bezeichner für den-Rückruf als Teil der Verarbeitung dieser Nachricht zurück.

</dd> <dt>

<span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>Zeile \_ calldevspecific
</dt> <dd>

Gibt an, dass auf einem Telefongerät ein Geräte spezifisches Ereignis aufgetreten ist.

</dd> <dt>

<span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>LINE \_ calldevspecificfeature
</dt> <dd>

Gibt an, dass auf einem Telefongerät ein Geräte spezifisches Funktions Ereignis aufgetreten ist.

</dd> </dl>

 

 
