---
title: Hide-Methode
description: Hide-Methode
ms.assetid: c30eda78-0951-43b4-8ae1-daccbd41170d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67057464c8e505e56123f712d3a1e6d668c7d75b00bc4732e7b18195b3be9723
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725450"
---
# <a name="hide-method"></a>Hide-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Blendet das angegebene Zeichen aus.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_")._ *  \[ *Schnelles* Ausblenden\]



| Teil   | Beschreibung                                                                                                                                                                                                                                      |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Fast* | Optional. Ein boolescher Wert, der angibt, ob die Animation übersprungen werden soll, die dem Hiding-Status **true** des Zeichens zugeordnet ist. Die **Ausblenden-Animation** wird nicht wiedergegeben. <br/> **False** (Standard) Gibt die **Ausblenden-Animation wieder.** <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Server reiht die Aktionen der **Hide-Methode** in die Warteschlange des Zeichens ein, sodass Sie es verwenden können, um das Zeichen nach einer Sequenz anderer Animationen auszublenden. Sie können die Aktion sofort mithilfe der [**Stop-Methode**](stop-method.md) wiedergeben, bevor Sie diese Methode aufrufen.

Wenn Sie einen Objektverweis deklarieren und auf diese Methode festlegen, wird ein [**Request-Objekt**](/windows/desktop/lwef/the-request-object) zurückgegeben. Wenn die zugeordnete **Hiding-Animation** nicht geladen wurde und Sie den **Fast-Parameter** nicht als **True** angegeben haben, legt der Server außerdem die [**Eigenschaft**](status-property.md) Status des **Anforderungsobjekts** auf "Failed" mit einer entsprechenden Fehlernummer fest. Wenn Sie das HTTP-Protokoll für den Zugriff auf Zeichen- oder Animationsdaten verwenden, verwenden Sie daher die Get-Methode, und geben [**Sie**](get-method.md) den **Hiding-Zustand** an, um die Animation zu laden, bevor Sie die **Hide-Methode** aufrufen.

Das Ausblenden eines Zeichens kann auch dazu führen, dass das [**ActivateInput-Ereignis**](activateinput-event.md) eines anderen Clients ausgelöst wird.

> [!Note]  
> Ausgeblendete Zeichen können nicht auf den Audiokanal zugreifen. Der Server übergibt einen Fehlerstatus im [**RequestComplete-Ereignis**](requestcomplete-event.md) zurück, wenn Sie eine Animationsanforderung generieren und das Zeichen ausgeblendet ist.

 

## <a name="see-also"></a>Weitere Informationen

[**Show-Methode**](show-method.md)


 

