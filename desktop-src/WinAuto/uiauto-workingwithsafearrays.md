---
title: Bewährte Methoden für die Verwendung von sicheren Arrays
description: Viele Schnittstellen Methoden der Microsoft UI Automation \ 32; API übernimmt Argumente, die als sichere Arrays bezeichnet werden, des SAFEARRAY-Datentyps. In diesem Thema werden die bewährten Methoden für die Verwendung von sicheren Arrays in Benutzeroberflächenautomatisierungs-Anwendungen beschrieben.
ms.assetid: 07e87cfd-d565-41b5-a68d-b99dd191fa95
keywords:
- Benutzeroberflächen Automatisierung, sichere Arrays
- Benutzeroberflächen Automatisierung, Anbieter
- Benutzeroberflächen Automatisierung, Clients
- Automatisierung der Benutzeroberfläche, umrechnen zwischen Datentypen
- Clients, sichere Arrays
- Anbieter, Benutzeroberflächen Automatisierung
- sichere Arrays
- Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ade30398f8fbeb43336707f66a0709dfab83d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337453"
---
# <a name="best-practices-for-using-safe-arrays"></a>Bewährte Methoden für die Verwendung von sicheren Arrays

Viele Schnittstellen Methoden der Microsoft UI Automation API akzeptieren Argumente, die als sichere Arrays bezeichnet werden, des [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) -Datentyps. In diesem Thema werden die bewährten Methoden für die Verwendung von sicheren Arrays in Benutzeroberflächenautomatisierungs-Anwendungen beschrieben.

## <a name="clients"></a>Clients

Alle sicheren Arrays, die mit den Benutzeroberflächenautomatisierungs-Client-API-Methoden verwendet werden, sind null basierte, eindimensionale Arrays. Um ein sicheres Array für eine Benutzeroberflächenautomatisierungs-Client Methode zu erstellen, verwenden Sie die [**safearraykreatevector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) -Funktion, und verwenden Sie zum Lesen und Schreiben in ein sicheres Array die Funktionen [**safearraygetelement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) und [**safearrayputelement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) . Wenn Sie die Verwendung eines sicheren Arrays abgeschlossen haben, sollten Sie es immer mit der [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) -Funktion zerstören, unabhängig davon, ob Sie das sichere Array erstellt oder von einer Benutzeroberflächenautomatisierungs-Client Methode empfangen haben.

Mehrere Methoden zur Benutzeroberflächen Automatisierung, einschließlich Eigenschaften Abruf Methoden wie z. b. [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), rufen [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant)s ab, die [**Punkt**](/previous-versions//dd162805(v=vs.85)) -oder [**uiarect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) -Strukturen enthalten können. Ein **Punkt** wird in eine **Variante** als sicheres Array von Doubles (VT \_ R8) mit dem **x** -Member an Index 0 und dem **y** -Element bei Index 1 verpackt. Analog dazu wird **ein uiarect** in eine **Variante** als sicheres Array von Double-Elementen mit den Elementen **left**, **Top**, **Width** und **height** bei den Indizes 0 bis 3 verpackt. Für ein Array von **uiarect** -Strukturen enthält das sichere Array ein sequenzielles Array von vier Doubles für jeden **uiarect**. Die Elemente **left**, **Top**, **Width** und **height** des ersten **uiarect** belegen den Index 0 bis 3, die Elemente des zweiten Rechtecks belegen den Index 4 bis 7 usw.

Die [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) -Schnittstelle umfasst die folgenden Methoden für die Typumwandlung zwischen [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) und verschiedenen anderen Datentypen.



| Methode                                                                                               | BESCHREIBUNG                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**Iuiautomation:: intnativearrayto SAFEARRAY**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray)   | Konvertiert ein Array von ganzen Zahlen in ein [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).                                          |
| [**Iuiautomation:: inzafearraytonativearray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray)   | Konvertiert ein [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) von ganzen Zahlen in ein Array.                                          |
| [**Iuiautomation:: safearraytor ectnativearray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray) | Konvertiert ein [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) , das Rechteck Koordinaten enthält, in ein Array vom Typ " **Rect**". |



 

## <a name="providers"></a>Anbieter

Ein Anbieter muss eine Reihe von Schnittstellen Methoden implementieren, die von der Benutzeroberflächen Automatisierung aufgerufen werden, um Informationen vom Anbieter abzurufen. Viele Male bestehen diese Informationen aus einem Array von Werten. Zum Zurückgeben eines Arrays an die Benutzeroberflächen Automatisierung muss der Anbieter das Array in eine [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) -Struktur packen. Die Array Elemente müssen den erwarteten Datentyp aufweisen und müssen in der erwarteten Reihenfolge angezeigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften](uiauto-propertiesoverview.md)
</dt> <dt>

[Grundlagen der Benutzeroberflächenautomatisierung](entry-uiautocore-overview.md)
</dt> </dl>

 

 