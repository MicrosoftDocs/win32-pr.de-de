---
title: FontName-Eigenschaft (Commands-Objekt)
description: FontName-Eigenschaft
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b04fa386958a75b55f9cfc50a9149de454d48f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102731"
---
# <a name="fontname-property-commands-object"></a>FontName-Eigenschaft (Commands-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die im Popupmenü des Zeichens verwendete Schriftart zurück oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent. *-**Zeichen ("**_Merkmal-ID_*_"). "Commands. FontName_"- *  \[  =  *Schriftart*\]



| Teil   | BESCHREIBUNG                                      |
|--------|--------------------------------------------------|
| *Schriftart* | Ein Zeichen folgen Wert, der dem Namen der Schriftart entspricht. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **FontName** -Eigenschaft definiert die Schriftart, die zum Anzeigen von Text im Popupmenü des Zeichens verwendet wird. Der Standardwert für die Schriftart Einstellung basiert auf der Einstellung für die Einstellung der Schriftart für die **LanguageID** -Einstellung des Zeichens, oder--wenn dies nicht festgelegt ist, der Standardeinstellung für die Benutzer-ID der Benutzereinstellung.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

 

 




