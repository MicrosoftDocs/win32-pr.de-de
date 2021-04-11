---
description: Erstellt ein generisches Transaktions Objekt, das eine Transaktion startet.
ms.assetid: efaf1468-4973-472f-af91-85957a52b7df
title: Transaktioncontext-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContext
api_type:
- COM
ms.openlocfilehash: 595b5a3192b87420855eb43f1e1e33df37a45c23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214260"
---
# <a name="transactioncontext-class"></a>Transaktioncontext-Klasse

Erstellt ein generisches Transaktions Objekt, das eine Transaktion startet. Indem Sie die Methoden dieser Klasse aufrufen, können Sie die Arbeit mehrerer COM-Objekte in einer einzelnen Transaktion verfassen und die Transaktion explizit Committe oder Abbrechen.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von com+ implementiert.



| Anforderung | Wert |
|------------|----------------------------------------------------|
| CLSID      | CLSID- \_ Transaktionskontext                          |
| ProgID     | L "txctx. transaktioncontext"                        |
| Schnittstellen | [**Itransaktioncontext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext) |



 

## <a name="when-to-use"></a>Verwendung

Ein nicht transaktionaler Client verwendet diese Klasse, um eine Transaktion zu starten. Mithilfe der Methoden dieser Klasse kann der Client zusätzliche com-Objekte abrufen, die, wenn Sie für die Teilnahme an einer Transaktion konfiguriert sind, innerhalb der Transaktions Begrenzung des Transaktionskontext Objekts ausgeführt werden. Basierend auf der Geschäftslogik kann der Client den Commit für die Transaktion explizit durchsetzen oder Abbrechen.

Die **transaktioncontext** -Klasse schränkt die Wiederverwendung der Geschäftslogik ein, die die Transaktion steuert. Aus diesem Grund wird empfohlen, dass Objekte, die von der **transaktioncontext** -Klasse instanziiert werden, sparsam verwendet werden.

## <a name="remarks"></a>Bemerkungen

Um dieses Objekt zu erstellen, rufen Sie [**IObjectContext:: kreateinstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)auf.

Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu. Ein transaktioncontext-Objekt kann mithilfe von "COMSVCSLIB. transaktioncontext" als Klassenname deklariert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>"Comsvcs. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Konfigurieren von Transaktionen](configuring-transactions.md)
</dt> <dt>

[**Itransaktioncontext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext)
</dt> <dt>

[**Transaction contextex**](transactioncontextex.md)
</dt> </dl>

 

 




