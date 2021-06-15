---
title: HelpContextID-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die HelpContextID-Eigenschaft des Characters-Objekts. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e751cb2d8834a6af2c3b816066d6051e3a28c767
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068186"
---
# <a name="helpcontextid-property-characters-object"></a>HelpContextID-Eigenschaft (Characters-Objekt)

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt eine zugeordnete Kontextnummer für das Zeichen zurück oder legt diese fest. Wird verwendet, um kontextsensitive Hilfe für das Zeichen zur Verfügung zu stellen.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). HelpContextID-Nummer_ *  \[  =  \]



| Teil     | BESCHREIBUNG                                   |
|----------|-----------------------------------------------|
| *Number* | Eine ganze Zahl, die eine gültige Kontextnummer angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um kontextorientierte Hilfe für das Zeichen zu unterstützen, weisen Sie die Kontextnummer dem Zeichen zu, das Sie beim Kompilieren der Hilfedatei für das zugehörige Hilfethema verwenden. Diese Eigenschaft gilt nur für den Client des Zeichens. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen des Clients aus.

Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile-Eigenschaft**](helpfile-property.md) des Zeichens festgelegt haben, ruft der -Agent die Hilfe automatisch auf, wenn [**HelpModeOn**](helpmodeon-property.md) auf **True** festgelegt ist und der Benutzer auf das Zeichen klickt. Wenn die [**HelpContextID**](helpcontextid-property.md)eine Kontextnummer enthält, ruft der -Agent die Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontextnummer identifiziert wird. Die aktuelle Kontextnummer ist der Wert von **HelpContextID** für das Zeichen.

> [!Note]  
> Zum Erstellen einer Hilfedatei ist der Microsoft Windows-Hilfecompiler erforderlich.

 

## <a name="see-also"></a>Weitere Informationen

[**HelpFile-Eigenschaft**](helpfile-property.md)


 

 




