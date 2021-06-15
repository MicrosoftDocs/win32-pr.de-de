---
title: HelpContextID-Eigenschaft (Befehlsobjekt)
description: Erfahren Sie mehr über die HelpContextID-Eigenschaft des Command-Objekts. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461c3c0ff5a6722dd6740c7df7e89bf2b9520053
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068511"
---
# <a name="helpcontextid-property-command-object"></a>HelpContextID-Eigenschaft (Befehlsobjekt)

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt eine zugeordnete Kontextnummer für das Command-Objekt zurück [**oder legt diese**](/windows/desktop/lwef/the-command-object) fest. Wird verwendet, um kontextsensitive Hilfe für das **Command-Objekt** zur Verfügung zu stellen.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands(""). HelpContextID-Nummer_ *  \[  =  \]



| Teil     | BESCHREIBUNG                                   |
|----------|-----------------------------------------------|
| *Number* | Eine ganze Zahl, die eine gültige Kontextnummer angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile-Eigenschaft**](helpfile-property.md) des Zeichens auf die Datei festgelegt haben, ruft der -Agent die Hilfe automatisch auf, wenn [**HelpModeOn**](helpmodeon-property.md) auf True festgelegt ist und der Benutzer den Befehl auswählt.  Wenn Sie eine Kontextnummer in [**helpContextID**](helpcontextid-property.md)festlegen, ruft der -Agent die Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontextnummer identifiziert wird. Die aktuelle Kontextnummer ist der Wert von **HelpContextID** für den Befehl.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

> [!Note]  
> Zum Erstellen einer Hilfedatei ist der Microsoft Windows-Hilfecompiler erforderlich.

 

## <a name="see-also"></a>Weitere Informationen

[**HelpFile-Eigenschaft**](helpfile-property.md)


 

 
