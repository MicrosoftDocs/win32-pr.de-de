---
title: HelpContextID-Eigenschaft (Commands Collection-Objekt)
description: Erfahren Sie mehr über die HelpContextID-Eigenschaft des Commands Collection-Objekts. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ed6ccf40545e15b3603ce5abe80ef94ff4272a
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068236"
---
# <a name="helpcontextid-property-commands-collection-object"></a>HelpContextID-Eigenschaft (Commands Collection-Objekt)

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt eine zugeordnete Kontextnummer für das Commands-Objekt zurück oder [**legt**](/windows/desktop/lwef/the-commands-collection-object) diese fest. Wird verwendet, um kontextsensitive Hilfe für das **Commands-Objekt** zur Verfügung zu stellen.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands("_*_name_*_"). HelpContextID-Nummer_ *  \[  =  \]



| Teil     | BESCHREIBUNG                                   |
|----------|-----------------------------------------------|
| *Number* | Eine ganze Zahl, die eine gültige Kontextnummer angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile-Eigenschaft**](helpfile-property.md) des Zeichens festgelegt haben, ruft der -Agent die Hilfe automatisch auf, wenn [**HelpModeOn**](helpmodeon-property.md) auf **True** festgelegt ist und der Benutzer das [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) auswählt. Wenn Sie eine Kontextnummer in **helpContextID** festlegen, ruft der -Agent die Hilfe auf und sucht nach dem Thema, das durch diese Kontextnummer identifiziert wird.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

> [!Note]  
> Zum Erstellen einer Hilfedatei ist der Microsoft Windows-Hilfecompiler erforderlich.

 

## <a name="see-also"></a>Weitere Informationen

[**HelpFile-Eigenschaft**](helpfile-property.md)


 

 
