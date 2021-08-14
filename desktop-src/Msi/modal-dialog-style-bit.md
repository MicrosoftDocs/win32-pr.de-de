---
description: Wenn dieses Bit festgelegt ist, ist das Dialogfeld modal, andere Dialoge derselben Anwendung können nicht darauf gesetzt werden, und der Dialog behält das Steuerelement bei der Ausführung bei.
ms.assetid: 14871dc7-c928-4381-a043-6beb06d25214
title: Modale Dialogformatbits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3663445a81acf07aebd9961f8ddb048dc8c8f466968573ac2c45544d6bd79baa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945477"
---
# <a name="modal-dialog-style-bit"></a>Modale Dialogformatbits

Wenn dieses Bit festgelegt ist, ist das Dialogfeld modal, andere Dialoge derselben Anwendung können nicht darauf gesetzt werden, und der Dialog behält das Steuerelement bei der Ausführung bei. Wenn dieses Bit nicht festgelegt ist, ist der Dialog moduslos, andere Dialoge derselben Anwendung können darüber verschoben werden. Nachdem ein modusloser Dialog erstellt und angezeigt wurde, gibt die Benutzeroberfläche die Steuerung an das Installationsprogramm zurück. Das Installationsprogramm ruft dann die Benutzeroberfläche in regelmäßigen Abständen auf, um den Dialog zu aktualisieren und ihm die Möglichkeit zu geben, die Nachrichten zu verarbeiten. Sobald dies erfolgt ist, wird das Steuerelement an das Installationsprogramm zurückgegeben.

> [!Note]  
> Es sollten keine moduslosen Dialoge in einer Assistentensequenz enthalten sein, da dies die Steuerung an das Installationsprogramm zurückgeben und die Assistentensequenz vorzeitig beenden würde.

 

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbDialogAttributesSysModal** |



 

 

 



