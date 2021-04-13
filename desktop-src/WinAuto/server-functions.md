---
title: Server Funktionen (Barrierefreiheits Funktionen von Windows)
description: Server Funktionen
ms.assetid: 3cfa42c4-3d8b-44a1-9b8e-19248da12334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10a747c073e84049fe578d19561b25d0b754dbb9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391472"
---
# <a name="server-functions-windows-accessibility-features"></a>Server Funktionen (Barrierefreiheits Funktionen von Windows)

Dieser Abschnitt enthält Informationen zu den-Serverfunktionen, die mit Microsoft Active Accessibility verwendet werden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Accnotifytouchinteraktion**](/windows/desktop/api/Oleacc/nf-oleacc-accnotifytouchinteraction)<br/> | Ermöglicht es einer Anwendung für Hilfstechnologien (at), das System zu benachrichtigen, dass die Interaktion mit der Benutzeroberfläche über eine Windows-Automatisierungs-API (z. b. Microsoft UI Automation) als Ergebnis einer touchbewegung vom Benutzer erfolgt. Dadurch kann die Hilfstechnologie die Zielanwendung und das System Benachrichtigen, mit dem der Benutzer interagiert.<br/> |
| [**Accabtrunningutilitystate**](/windows/desktop/api/Oleacc/nf-oleacc-accsetrunningutilitystate)<br/> | Legt System Werte fest, die angeben, ob sich der aktuelle Zustand einer Hilfstechnologie (at) auf Funktionen auswirkt, die normalerweise vom System bereitgestellt werden. <br/>                                                                                                                                                                                 |
| [**"Kreatestdaccessibleobject"**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject)<br/> | Erstellt ein Barrierefreies Objekt mit den Methoden und Eigenschaften des angegebenen Typs des vom System bereitgestellten Benutzeroberflächen Elements.<br/>                                                                                                                                                                                                                      |
| [**"Kreatestdaccessibleproxy"**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya)<br/>   | Erstellt ein Barrierefreies Objekt, das über die Eigenschaften und Methoden der angegebenen Klasse des vom System bereitgestellten Benutzeroberflächen Elements verfügt.<br/>                                                                                                                                                                                                                 |
| [**Lresultfromobject.**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)<br/>                 | Gibt dem angegebenen Objekt einen Verweis ähnlich einem Handle zurück. Server geben diesen Verweis zurück, wenn Sie [**WM \_ GetObject**](wm-getobject.md)verarbeiten.<br/>                                                                                                                                                                                              |
| [**Objectfromlresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult)<br/>                 | Ruft einen angeforderten Schnittstellen Zeiger für ein Barrierefreies Objekt auf Grundlage eines zuvor generierten Objekt Verweises ab.<br/> Diese Funktion ist für die interne Verwendung durch Microsoft Active Accessibility konzipiert und wird nur für Informationszwecke dokumentiert. Diese Funktion sollte weder von Clients noch von Servern aufgerufen werden.<br/>                               |
| [**Iswineventhookinangeh alten**](/windows/desktop/api/Winuser/nf-winuser-iswineventhookinstalled)<br/>     | Bestimmt, ob ein installierter WinEvent-Hook vorhanden ist, der möglicherweise über ein angegebenes Ereignis benachrichtigt wird.<br/>                                                                                                                                                                                                                                                |
| [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)<br/>                       | Signalisiert dem System, dass ein vordefiniertes Ereignis aufgetreten ist. Wenn Client Anwendungen eine Hook-Funktion für das Ereignis registriert haben, ruft das System die Hook-Funktion des Clients auf.<br/>                                                                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Active Accessibility von Benutzeroberflächen Diensten](active-accessibility-user-interface-services-ref.md)
</dt> </dl>

 

 





