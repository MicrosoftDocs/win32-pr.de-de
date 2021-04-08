---
description: Erstellt ein generisches Transaktions Objekt, das eine Transaktion startet. Indem Sie die Methoden dieser Klasse aufrufen, können Sie die Arbeit mehrerer COM-Objekte in einer einzelnen Transaktion verfassen und die Transaktion explizit Committe oder Abbrechen.
ms.assetid: 5f3f83e0-33fc-4c43-9327-59485c0d8bd3
title: Transaction contextex-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContextEx
api_type:
- COM
ms.openlocfilehash: 8cf5c3aaa7ffe126124a909498a7c54cfb012c65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748840"
---
# <a name="transactioncontextex-class"></a>Transaction contextex-Klasse

Erstellt ein generisches Transaktions Objekt, das eine Transaktion startet. Indem Sie die Methoden dieser Klasse aufrufen, können Sie die Arbeit mehrerer COM-Objekte in einer einzelnen Transaktion verfassen und die Transaktion explizit Committe oder Abbrechen.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von com+ implementiert.



| Anforderung | Wert |
|------------|--------------------------------------------------------|
| CLSID      | CLSID \_ Transaction contextex                            |
| ProgID     | L "txctx. Transaction contextex"                          |
| Schnittstellen | [**ITransaction contextex**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex) |



 

## <a name="when-to-use"></a>Verwendung

Ein nicht transaktionaler Client verwendet diese Klasse, um eine Transaktion zu starten. Mithilfe der Methoden dieser Klasse kann der Client zusätzliche com-Objekte abrufen, die, wenn Sie für die Teilnahme an einer Transaktion konfiguriert sind, innerhalb der Transaktions Begrenzung des Transaktionskontext Objekts ausgeführt werden. Basierend auf der Geschäftslogik kann der Client den Commit für die Transaktion explizit durchsetzen oder Abbrechen.

Die **Transaction contextex** -Klasse schränkt die Wiederverwendung der Geschäftslogik ein, die die Transaktion steuert. Aus diesem Grund wird empfohlen, dass Objekte, die von der **Transaction contextex** -Klasse instanziiert werden, sparsam verwendet werden.

## <a name="remarks"></a>Bemerkungen

Um dieses Objekt zu erstellen, rufen Sie [**IObjectContext:: kreateinstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)auf.

Die **Transaction contextex** -Klasse wurde nicht für die Verwendung in Visual Basic konzipiert. Verwenden Sie stattdessen die [**transaktioncontext**](transactioncontext.md) -Klasse.

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

[**ITransaction contextex**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex)
</dt> <dt>

[**Transaktioncontext**](transactioncontext.md)
</dt> </dl>

 

 




