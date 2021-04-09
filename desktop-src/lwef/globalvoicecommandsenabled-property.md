---
title: Globalvoicecommandsenabled (Eigenschaft)
description: Globalvoicecommandsenabled (Eigenschaft)
ms.assetid: d4f74019-fa33-41fc-abe7-01791ff188f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f523171187c9956a7741afc0fabcc7ec794071
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948751"
---
# <a name="globalvoicecommandsenabled-property"></a>Globalvoicecommandsenabled (Eigenschaft)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück oder legt fest, ob Voice für die globalen Befehle des Agents aktiviert ist.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Büros. ***Zeichen ("*** Merkmal-ID * * *"). Commands. globalvoicecommandsenabled**

\[ = *booleschen*\]



| Teil      | BESCHREIBUNG                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der angibt, ob sprach Parameter für die globalen Befehle des Agents aktiviert sind. **True** (Standard) sprach Parameter sind aktiviert. <br/> **False** Sprach Parameter sind deaktiviert.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Microsoft-Agent fügt automatisch sprach Parameter (Grammatik) zum Öffnen und Schließen des Sprachbefehle Fensters und zum ein-und Ausblenden des Zeichens hinzu. Wenn Sie **globalvoicecommandsenabled** auf **false** festlegen, deaktiviert der-Agent alle sprach Parameter für diese Befehle sowie die sprach Parameter für die [**Beschriftung**](caption-property.md) der [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Objekte anderer Clients. Dies ermöglicht es Ihnen, diese aus der aktuellen aktiven Grammatik Ihres Clients auszuschließen. Da dadurch jedoch möglicherweise der sprach Zugriff auf andere Clients blockiert wird, setzen Sie diese Eigenschaft nach dem Verarbeiten der Spracheingabe des Benutzers auf " **true** " zurück.

Das Deaktivieren der Eigenschaft wirkt sich nicht auf das Popup Menü des Zeichens aus. Die vom Server hinzugefügten globalen Befehle werden weiterhin angezeigt. Sie können Sie nicht aus dem Popupmenü entfernen.

 

