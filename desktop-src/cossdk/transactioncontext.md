---
description: Erstellt ein generisches Transaktionsobjekt, das eine Transaktion startet.
ms.assetid: efaf1468-4973-472f-af91-85957a52b7df
title: TransactionContext-Klasse (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContext
api_type:
- COM
ms.openlocfilehash: aa0a90cee2b0af7d5ebe3679dca46aa04c6326fb5fd62fe5f57699d610b9efe8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678150"
---
# <a name="transactioncontext-class"></a>TransactionContext-Klasse

Erstellt ein generisches Transaktionsobjekt, das eine Transaktion startet. Durch Aufrufen der Methoden dieser Klasse können Sie die Arbeit mehrerer COM-Objekte in einer einzelnen Transaktion zusammenstellen und die Transaktion explizit committen oder abbrechen.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von COM+ implementiert.



| Anforderung | Wert |
|------------|----------------------------------------------------|
| CLSID      | CLSID \_ TransactionContext                          |
| ProgID     | L"TxCTx.TransactionContext"                        |
| Schnittstellen | [**ITransactionContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext) |



 

## <a name="when-to-use"></a>Verwendung

Ein nicht transaktionaler Client verwendet diese Klasse, um eine Transaktion zu starten. Mithilfe der Methoden dieser Klasse kann der Client zusätzliche COM-Objekte aufrufen, die innerhalb der Transaktionsgrenze des Transaktionskontextobjekts ausgeführt werden, wenn sie für die Teilnahme an einer Transaktion konfiguriert sind. Basierend auf seiner Geschäftslogik kann der Client die Transaktion explizit committen oder abbrechen.

Die **TransactionContext-Klasse** schränkt die Wiederverwendung der Geschäftslogik ein, die die Transaktion antreibt. Aus diesem Grund wird empfohlen, objekte, die aus der **TransactionContext-Klasse** instanziiert wurden, nur selten zu verwenden.

## <a name="remarks"></a>Hinweise

Um dieses Objekt zu erstellen, rufen [**Sie IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)auf.

Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die COM+-Diensttypbibliothek hinzu. Ein TransactionContext-Objekt kann mit "COMSVCSLib.TransactionContext" als Klassenname deklariert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Konfigurieren von Transaktionen](configuring-transactions.md)
</dt> <dt>

[**ITransactionContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext)
</dt> <dt>

[**TransactionContextEx**](transactioncontextex.md)
</dt> </dl>

 

 




