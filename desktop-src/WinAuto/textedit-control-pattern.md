---
title: TextEdit-Steuerelement Muster
description: Führt Richtlinien und Konventionen für das Implementieren von itexteditprovider ein, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: AA9E04AC-1AC0-6434-ADEF-9FF82ADA7CD9
keywords:
- Benutzeroberflächen Automatisierung, Implementieren des TextEdit-Steuerelement Musters
- Benutzeroberflächenautomatisierungs-Steuerelement Muster
- Steuerelement Muster, TextEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf8512db4f676a263bf46bdbdfea7b6b7eaba11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316347"
---
# <a name="textedit-control-pattern"></a>TextEdit-Steuerelement Muster

Führt Richtlinien und Konventionen für das Implementieren von [**itexteditprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider)ein, einschließlich Informationen zu Eigenschaften und Methoden. Das **TextEdit** -Steuerelement Muster wird für den programmgesteuerten Zugriff auf ein Steuerelement verwendet, das Text ändert, z. b. ein Steuerelement, das die automatische Korrektur durchführt oder die Eingabe Komposition ermöglicht.

> [!Note]  
> Die Implementierungs Hinweise in diesem Thema beziehen sich auf APIs, die aus dem Text Services-Framework (TSF) stammen. Weitere Informationen zu TSF und der API-Referenz finden Sie unter [Text Services-Framework](/windows/desktop/TSF/text-services-framework).

 

## <a name="required-members-for-itexteditprovider"></a>Erforderliche Member für **itexteditprovider**

Diese Eigenschaften und Methoden sind für die Implementierung der [**itexteditprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                              | Memberart | Hinweise                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getactivecomposition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getactivecomposition) | Methode      | Gibt den Bereich der aktuellen Konvertierung zurück (None, wenn keine Konvertierung vorhanden ist). Gibt die aktive Komposition zurück (in TSF ist dies der Bereich, der durch **GUID- \_ Prop- \_ Komposition** gekennzeichnet ist). Beispielsweise ist der Microsoft-Eingabemethoden-Editor (IME) der vollständig unterstrichene Text. |
| [**Getsubversiontarget**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getconversiontarget)   | Methode      | Gibt den aktuellen Konvertierungs Zielbereich zurück (None, wenn keine Konvertierung durchführt). In TSF ist dies der Bereich von Zeichen, die als **tf \_ attr \_ Target \_ notumgerechnet** oder **tf \_ attr \_ Target \_** gekennzeichnet sind, das aus der **tf \_ DisplayAttribute** -Struktur konvertiert wurde.                                               |



 

Die Ereignisse " **textedittextchanged** " und " **konversiontargetchanged** " müssen von Microsoft UI Automation-Elementen ausgelöst werden, die das **TextEdit** -Muster unterstützen.

### <a name="textedittextchanged"></a>**Textedittextchanged**

-   Verwenden Sie die [**uiaraiabtextedittextchangedebug**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) -Funktion, um das **textedittextchanged** -Ereignis auszulösen.
-   In der folgenden Tabelle sind die Fälle aufgeführt, in denen das-Ereignis und die [**uiaraiabtextedittextchangedevent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) -Parameter für die Verwendung von ausgelöst werden sollten.



| Texteditchangetype                                            | Ereignisnutzlast                                | Notizen                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutoKorrektur**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | Neue korrigierte Zeichenfolge                         | Wird ausgelöst, wenn das Steuerelement eine automatische Korrektur durchgeführt hat. Oder wenn eine Ersetzung durch TSF erfolgt und der Bereich einen **GUID- \_ Prop- \_ TKB \_** -Wert aufweist, wird die **\_ \_ Automatische Korrektur \_ angewendet**.<br/>                                                                                                                                                                   |
| [**Aufbau**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | Die aktualisierte Zeichenfolge                           | Die Nutzlast darf nur die Zeichen enthalten, die sich geändert haben (die gesamte Kompositions Zeichenfolge nicht senden). Wird immer dann ausgelöst, wenn ein Kompositions Austausch erfolgt. In TSF wird ein Kompositions Austausch als Ersatz definiert, bei dem das Flag für die **GUID- \_ Prop- \_ Komposition** festgelegt ist. Bearbeitungs Steuerelemente, die TSF implementieren, können diese Änderungen über die **onendedit** -Benachrichtigung überwachen.<br/>         |
| [**Compositionfinalisiert**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype) | Die fertige Kompositions Zeichenfolge (siehe Hinweise) | In TSF wird die Konvertierungs Zeichenfolge, die abgeschlossen wird, von dem **GUID- \_ \_** Bestellungs Flag definiert, das aus einer Komposition entfernt wird. Bearbeitungs Steuerelemente, die TSF implementieren, sollten die fertige Zeichenfolge aus **endcomposition** ermitteln und das-Ereignis beim Aufrufen von **onendedit** erhöhen.<br/> Die abgeschlossene Kompositions Zeichenfolge ist möglicherweise leer, wenn die Komposition abgebrochen oder gelöscht wurde.<br/> |



 

### <a name="conversiontargetchanged"></a>**"Systemversiontargetchanged"**

-   " **Konversiontargetchanged** " tritt auf, wenn sich das Konvertierungs Ziel von einem Ziel in ein anderes ändert
-   Verwenden Sie die [**uiaraitarautomationevent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent) -Funktion, **um das Ereignis** "Ereignis" in der Ereignis Umgebung " [**UIA \_ TextEdit \_**](https://www.bing.com/search?q=**UIA\_TextEdit\_ConversionTargetChangedEventId**) " zu auslösen.
-   " **Subversiontargetchanged** " sollte nicht ausgelöst werden, wenn der Inhalt des Ziels geändert wird. Wenn die Ziel Änderung gleichzeitig mit einer Kompositions Änderung erfolgt, muss das Ziel Änderungs Ereignis ausgelöst werden, nachdem bereits Kompositions Ereignisse ausgelöst wurden.
-   In TSF wird das Konvertierungs Ziel durch den Wert **tf \_ attr \_ Target \_** definiert, der aus der **tf \_ DisplayAttribute** -Struktur festgelegt wird. Änderungen können mithilfe von **onendedit** überwacht werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

