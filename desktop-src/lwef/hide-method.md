---
title: Hide-Methode
description: Hide-Methode
ms.assetid: c30eda78-0951-43b4-8ae1-daccbd41170d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd50c3f7b8e3d2e60ebe4c00c42375737c05eb04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101566"
---
# <a name="hide-method"></a>Hide-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Blendet das angegebene Zeichen aus.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *").* *  \[ *Schnell* ausblenden\]



| Teil   | BESCHREIBUNG                                                                                                                                                                                                                                      |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Fast* | Dies ist optional. Ein boolescher Wert, der angibt, ob die Animation übersprungen werden soll, die mit dem Ausblenden des Zeichens verknüpft ist. **true** gibt die **versteckte** Animation nicht wieder. <br/> **False** (Standard) gibt die **versteckte** Animation wieder. <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Server fügt die Aktionen der **Hide** -Methode in die Warteschlange des Zeichens ein, damit Sie das Zeichen nach einer Sequenz anderer Animationen ausblenden können. Sie können die Aktion sofort wiedergeben, indem Sie die Methode " [**Ende**](stop-method.md) " verwenden, bevor Sie diese Methode aufrufen.

Wenn Sie einen Objekt Verweis deklarieren und diesen auf diese Methode festlegen, wird ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückgegeben. Wenn die zugeordnete Ausblenden der **Animation nicht** geladen wurde und Sie den **fast** -Parameter nicht als **true** angegeben haben, legt der Server die Eigenschaft **Anforderungs** Objekt [**Status**](status-property.md) auf "failed" (Fehler) mit einer entsprechenden Fehlernummer fest. Wenn Sie also das HTTP-Protokoll für den Zugriff auf Zeichen-oder Animationsdaten verwenden, verwenden Sie die [**Get**](get-method.md) -Methode, und geben Sie den ausblenden **Status zum** Laden der Animation an, bevor Sie die **Hide** -Methode aufrufen.

Das Ausblenden eines Zeichens kann auch dazu führen, dass das [**activateinput**](activateinput-event.md) -Ereignis eines anderen Clients ausgelöst wird.

> [!Note]  
> Versteckte Zeichen können nicht auf den Audiokanal zugreifen. Der Server übergibt einen Fehlerstatus im [**requestcomplete**](requestcomplete-event.md) -Ereignis zurück, wenn Sie eine Animations Anforderung generieren und das Zeichen ausgeblendet ist.

 

## <a name="see-also"></a>Weitere Informationen

[**Show-Methode**](show-method.md)


 

