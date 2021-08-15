---
title: HelpContextID-Eigenschaft (Befehlsobjekt)
description: Erfahren Sie mehr über die HelpContextID-Eigenschaft des Command-Objekts. Microsoft Agent ist ab 7 Windows veraltet.
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38d0f725c0c809c70fa77b89d3608f8e713fd968c33bfb0192c712f3613e91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478707"
---
# <a name="helpcontextid-property-command-object"></a>HelpContextID-Eigenschaft (Befehlsobjekt)

\[Microsoft Agent ist ab Version Windows 7 veraltet und möglicherweise in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt eine zugeordnete Kontextnummer für das Command-Objekt zurück oder [**legt diese**](/windows/desktop/lwef/the-command-object) fest. Wird verwendet, um kontextsensitive Hilfe für das **Command-Objekt** zur Verfügung zu stellen.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands(""). HelpContextID-Nummer_ *  \[  =  \]



| Teil     | BESCHREIBUNG                                   |
|----------|-----------------------------------------------|
| *Number* | Eine ganze Zahl, die eine gültige Kontextnummer angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile-Eigenschaft**](helpfile-property.md) des Zeichens auf die Datei festgelegt haben, ruft der -Agent die Hilfe automatisch auf, wenn [**HelpModeOn**](helpmodeon-property.md) auf **True** festgelegt ist und der Benutzer den Befehl auswählt. Wenn Sie eine Kontextnummer in [**helpContextID**](helpcontextid-property.md)festlegen, ruft der -Agent die Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontextnummer identifiziert wird. Die aktuelle Kontextnummer ist der Wert von **HelpContextID** für den Befehl.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

> [!Note]  
> Zum Erstellen einer Hilfedatei ist der Microsoft Windows Help Compiler erforderlich.

 

## <a name="see-also"></a>Weitere Informationen

[**HelpFile-Eigenschaft**](helpfile-property.md)


 

 
