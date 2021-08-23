---
title: DeactivateInput-Ereignis
description: DeactivateInput-Ereignis
ms.assetid: 59747932-82be-45d5-8465-73798904e8a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98fe94d7d4e737d83dfb734bcc5b35c60bddf96dcf8b07c43df3b89817da21b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610530"
---
# <a name="deactivateinput-event"></a>DeactivateInput-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn ein Client nicht eingabeaktiv wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Sub-Agent** \_ DeactivateInput* *  **(ByVal** *CharacterID))**



| Teil          | Beschreibung                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *CharacterID* | Gibt die ID des Zeichens zurück, durch das der Client nicht eingabeaktiv wird. |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Ein nicht eingabeaktiver Client empfängt keine Maus- oder Sprachereignisse mehr vom Server (es sei denn, er wird wieder eingabeaktiv). Der Server sendet dieses Ereignis nur an den Client, der nicht eingabeaktiv wird.

Dieses Ereignis tritt auf, wenn Ihre Clientanwendung eingabeaktiv ist und der Benutzer die Beschriftung eines anderen Clients im Popupmenü eines Zeichens oder im Fenster "Sprachbefehle" auswählt oder Sie die [**Activate-Methode**](activate-method.md) aufrufen und den **State-Parameter** auf 0 festlegen. Dies kann auch auftreten, wenn der Benutzer den Namen eines anderen Zeichens durch Klicken oder Sprechen auswählt. Sie erhalten dieses Ereignis auch, wenn Ihr Zeichen ausgeblendet ist oder ein anderes Zeichen sichtbar wird.

### <a name="see-also"></a>Weitere Informationen

[**ActivateInput-Ereignis**](activateinput-event.md)


 

 




