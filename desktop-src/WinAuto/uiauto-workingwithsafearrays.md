---
title: Bewährte Methoden für die Verwendung Tresor Arrays
description: Viele Schnittstellenmethoden des Microsoft Benutzeroberflächenautomatisierung \ 32; API-Take-Argumente, die als sichere Arrays bezeichnet werden, des SAFEARRAY-Datentyps. In diesem Thema werden die bewährten Methoden für die Verwendung sicherer Arrays in einer Benutzeroberflächenautomatisierung beschrieben.
ms.assetid: 07e87cfd-d565-41b5-a68d-b99dd191fa95
keywords:
- Benutzeroberflächenautomatisierung,sichere Arrays
- Benutzeroberflächenautomatisierung,providers
- Benutzeroberflächenautomatisierung,Clients
- Benutzeroberflächenautomatisierung,Konvertieren zwischen Datentypen
- Clients,sichere Arrays
- providers,Benutzeroberflächenautomatisierung
- Sichere Arrays
- Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ea76358f3a547b4364d01f56e850d0cbb523fc35dfbaa2870448f70c6ad5ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098120"
---
# <a name="best-practices-for-using-safe-arrays"></a>Bewährte Methoden für die Verwendung Tresor Arrays

Viele Schnittstellenmethoden der Microsoft Benutzeroberflächenautomatisierung-API verwenden Argumente, die als sichere Arrays bezeichnet werden, des [**SAFEARRAY-Datentyps.**](/windows/win32/api/oaidl/ns-oaidl-safearray) In diesem Thema werden die bewährten Methoden für die Verwendung sicherer Arrays in einer Benutzeroberflächenautomatisierung beschrieben.

## <a name="clients"></a>Clients

Alle sicheren Arrays, die mit den Benutzeroberflächenautomatisierung-API-Methoden verwendet werden, sind nullbasierte, eindimensionale Arrays. Um ein sicheres Array für eine Benutzeroberflächenautomatisierung-Clientmethode zu erstellen, verwenden Sie die [**SafeArrayCreateVector-Funktion**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) und zum Lesen und Schreiben in ein sicheres Array die [**SafeArrayGetElement-**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) und [**SafeArrayPutElement-Funktionen.**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) Wenn Sie die Verwendung eines sicheren Arrays abgeschlossen haben, zerstören Sie es immer mithilfe der [**SafeArrayDestroy-Funktion,**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) unabhängig davon, ob Sie das sichere Array erstellt oder von einer Benutzeroberflächenautomatisierung erhalten haben.

Mehrere Benutzeroberflächenautomatisierung, einschließlich Methoden zum Abrufen von Eigenschaften wie [**GetCurrentPropertyValue,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)rufen [**VARIANT-Elemente**](/windows/win32/api/oaidl/ns-oaidl-variant)ab, die [**POINT-**](/previous-versions//dd162805(v=vs.85)) oder [**UiaRect-Strukturen enthalten**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) können. Ein **POINT** wird als sicheres Array von Doubles (VT R8) mit dem x-Member bei Index 0 und dem y-Member an Index 1 in eine  \_ VARIANT-Datei gepackt.   Ebenso wird  ein **UiaRect** als sicheres Array von Doubles mit den  **linken,** oberen, breiten und Höhenmitgliedern an den Indizes 0 bis 3 in eine VARIANT-Gepackt.  Für ein Array von **UiaRect-Strukturen** enthält das sichere Array ein sequenzielles Array von vier Doubles für jedes **UiaRect-.** Die **linken,** **oberen,**  **Breiten-** und Höhenmitglieder des ersten **UiaRect** belegen Index 0 bis 3, die Elemente des zweiten Rechtecks belegen Index 4 bis 7 und so weiter.

Die [**IUIAutomation-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) enthält die folgenden Methoden zum Konvertieren zwischen [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) und verschiedenen anderen Datentypen.



| Methode                                                                                               | BESCHREIBUNG                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IUIAutomation::IntNativeArrayToSafeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray)   | Konvertiert ein Array von ganzen Zahlen in [**safearray**](/windows/win32/api/oaidl/ns-oaidl-safearray).                                          |
| [**IUIAutomation::IntSafeArrayToNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray)   | Konvertiert ein [**SAFEARRAY von**](/windows/win32/api/oaidl/ns-oaidl-safearray) ganzen Zahlen in ein Array.                                          |
| [**IUIAutomation::SafeArrayToRectNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray) | Konvertiert ein [**SAFEARRAY-Objekt,**](/windows/win32/api/oaidl/ns-oaidl-safearray) das Rechteckkoordinaten enthält, in ein Array vom **Typ RECT.** |



 

## <a name="providers"></a>Anbieter

Ein Anbieter muss eine Reihe von Schnittstellenmethoden implementieren, Benutzeroberflächenautomatisierung aufrufen, um Informationen vom Anbieter abzurufen. Diese Informationen bestehen oft aus einem Array von Werten. Um ein Array an Benutzeroberflächenautomatisierung zurücksingen zu können, muss der Anbieter das Array in eine [**SAFEARRAY-Struktur**](/windows/win32/api/oaidl/ns-oaidl-safearray) packen. Die Arrayelemente müssen den erwarteten Datentyp haben und in der erwarteten Reihenfolge angezeigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften](uiauto-propertiesoverview.md)
</dt> <dt>

[Grundlagen der Benutzeroberflächenautomatisierung](entry-uiautocore-overview.md)
</dt> </dl>

 

 