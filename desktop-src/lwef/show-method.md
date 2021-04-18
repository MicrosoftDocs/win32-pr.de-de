---
title: Show-Methode
description: Show-Methode
ms.assetid: 58adbb55-f4cb-4356-abc4-b85fa3af744d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05a1adaa46c85f34e02128960330c68d9a86db1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340486"
---
# <a name="show-method"></a>Show-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Macht das angegebene Zeichen sichtbar und gibt dessen zugeordnete **Animation wieder** .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *").* *  \[ *Schnell* anzeigen\]



| Teil   | BESCHREIBUNG                                                                                                                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Fast* | Dies ist optional. Ein boolescher Ausdruck, der angibt, ob der Server die **Anzeige** Animation wieder gibt. **True** Überspringt die **Anzeige** Status Animation. <br/> **False** (Standard) lässt die **Anzeige** Status Animation nicht überspringen. <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Objekt Verweis deklarieren und diesen auf diese Methode festlegen, wird ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückgegeben. Wenn außerdem die zugeordnete **Anzeige** Animation nicht geladen wurde und Sie den **fast** -Parameter nicht als **true** angegeben haben, legt der Server die [**Status**](status-property.md) -Eigenschaft des **Anforderungs** Objekts auf "failed" (Fehler) mit einer entsprechenden Fehlernummer fest. Wenn Sie also das HTTP-Protokoll verwenden, um auf **Daten der Zeichen** Animation zuzugreifen, verwenden Sie die [**Get**](get-method.md) -Methode, um die Show State-Animation vor dem Aufrufen der **Show** -Methode zu laden.

Legen Sie den **fast** -Parameter nicht auf " **true** " fest, ohne zuvor eine Animation vorher zu spielen Andernfalls wird der Zeichen Rahmen möglicherweise ohne Bild angezeigt. Beachten Sie insbesondere Folgendes: Wenn Sie " [**muveto**](moveto-method.md) " anrufen, wenn das Zeichen nicht sichtbar ist, wird keine Animation wiedergegeben. Wenn Sie also die **Show** -Methode aufrufen, bei der **fast** auf **true** festgelegt ist, wird kein Bild angezeigt. Wenn Sie " [**Ausblenden**](hide-method.md) **" und "mit** **fast** festgelegtem" auf " **true**" aufzurufen, wird das Bild nicht angezeigt.

## <a name="see-also"></a>Weitere Informationen

[**Hide-Methode**](hide-method.md)


 

