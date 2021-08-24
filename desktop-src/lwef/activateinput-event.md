---
title: ActivateInput-Ereignis
description: ActivateInput-Ereignis
ms.assetid: bc395750-5da0-4379-8eca-3195e936052c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db21d605a014002063a7c5aa42554a06adb1ed35296242944de789daeb3155c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610680"
---
# <a name="activateinput-event"></a>ActivateInput-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn ein Client eingabeaktiv wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Sub-Agent**  \_ ActivateInput **(ByVal** *CharacterID))**



| Teil          | Beschreibung                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *CharacterID* | Gibt die ID des Zeichens zurück, über das der Client eingabeaktiv wird. |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Der eingabeaktive Client empfängt vom Server bereitgestellte Maus- und Spracheingabeereignisse. Der Server sendet dieses Ereignis nur an den Client, der eingabeaktiv wird.

Dieses Ereignis kann auftreten, wenn der Benutzer zu Ihrem [Command-Objekt](the-command-object.md) wechselt, z. B. indem er im Befehlsfenster oder im Popupmenü für ein Zeichen den Eintrag Befehlsobjekt auswählt. Dies kann auch auftreten, wenn der Benutzer ein Zeichen auswählt (durch Klicken oder Sprechen seines Namens), wenn ein Zeichen sichtbar wird und das Zeichen einer anderen Clientanwendung ausgeblendet wird. Sie können auch die [Activate-Methode](activate-method.md) aufrufen (wobei **State** auf 2 festgelegt ist), um das Zeichen explizit an oberster Stelle zu setzen. Dies führt dazu, dass Ihre Clientanwendung eingabeaktiv wird und dieses Ereignis auslöst. Dieses Ereignis tritt jedoch nicht auf, wenn Sie die Methode Activate Method nur verwenden, um anzugeben, ob ihr Client der aktive Client des Zeichens ist.

### <a name="see-also"></a>Weitere Informationen

[**DeactivateInput-Ereignis,**](deactivateinput-event.md) [ **Activate-Methode**](activate-method.md)


 

 




