---
description: Wenn dieses Bit festgelegt ist, ist das Dialogfeld modal, andere Dialoge der gleichen Anwendung können nicht eingefügt werden, und im Dialogfeld wird das Steuerelement während der Ausführung beibehalten.
ms.assetid: 14871dc7-c928-4381-a043-6beb06d25214
title: Modales Dialog Feld Stilbit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd0004cc7b31557f9a606050a1f8569fa2a493d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529750"
---
# <a name="modal-dialog-style-bit"></a>Modales Dialog Feld Stilbit

Wenn dieses Bit festgelegt ist, ist das Dialogfeld modal, andere Dialoge der gleichen Anwendung können nicht eingefügt werden, und im Dialogfeld wird das Steuerelement während der Ausführung beibehalten. Wenn dieses Bit nicht festgelegt ist, ist das Dialogfeld "modeless", andere Dialoge der gleichen Anwendung können darauf verschoben werden. Nachdem ein nicht modalem Dialogfeld erstellt und angezeigt wurde, gibt die Benutzeroberfläche die Steuerung an das Installationsprogramm zurück. Das Installationsprogramm ruft dann die Benutzeroberfläche in regelmäßigen Abständen auf, um das Dialogfeld zu aktualisieren und die Möglichkeit zu haben, die Nachrichten zu verarbeiten. Sobald dies erfolgt ist, wird das Steuerelement an das Installationsprogramm zurückgegeben.

> [!Note]  
> In einer Assistenten Sequenz sollten keine modaldialogfelder vorhanden sein, da dadurch die Steuerung an das Installationsprogramm zurückgegeben wird, sodass die Assistenten Sequenz vorzeitig beendet wird.

 

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbdialogattributessysmodal** |



 

 

 



