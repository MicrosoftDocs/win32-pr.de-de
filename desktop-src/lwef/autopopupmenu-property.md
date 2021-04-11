---
title: Autopopupmenu (Eigenschaft)
description: Autopopupmenu (Eigenschaft)
ms.assetid: 499092cb-0990-4edb-915c-12e3011de142
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d4ebfc559c88c3750a338f30b5dee4aad66ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310807"
---
# <a name="autopopupmenu-property"></a>Autopopupmenu (Eigenschaft)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück oder legt fest, ob beim Klicken mit der rechten Maustaste auf das Zeichen oder das zugehörige Task leisten Symbol automatisch das Popup Menü des Zeichens angezeigt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent. ***Zeichen * * * * ("*** Merkmal-ID * * *"). Autopopupmenu*- *  \[  =  *boolescher* Wert\]



| Teil      | BESCHREIBUNG                                                                                                                                                                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der angibt, ob der Server beim Klicken mit der rechten Maustaste automatisch das Popup Menü des Zeichens anzeigt. **True** (Standard) zeigt das Menü mit der rechten Maustaste an. <br/> **False** Mit der rechten Maustaste wird das Menü nicht angezeigt.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie diese Eigenschaft auf " **false**" festlegen, können Sie ein eigenes Menü Verarbeitungs Verhalten erstellen. Verwenden Sie die [**showPopupMenu**](showpopupmenu-method.md) -Methode, um das Menü nach dem Festlegen dieser Eigenschaft auf **false** anzuzeigen.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**ShowPopupMenu-Methode**](showpopupmenu-method.md)


 

 





