---
title: Implementieren der Eigenschaften Seite für ein DSP-Plug-in
description: Implementieren der Eigenschaften Seite für ein DSP-Plug-in
ms.assetid: 3dd3e547-fd06-4f01-8731-da1f8c958a32
keywords:
- Windows Media Player-Plug-ins, audiodsp
- Plug-ins, audiodsp
- Plug-Ins für die digitale Signalverarbeitung, Audioeigenschaften
- DSP-Plug-ins, Audioeigenschaften
- audiodsp-Plug-ins, Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec87318b77fec4e9218398c1cb43dd5954a49e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855799"
---
# <a name="implementing-the-property-page-for-a-dsp-plug-in"></a>Implementieren der Eigenschaften Seite für ein DSP-Plug-in

Windows Media Player kann eine Eigenschaften Seite für jedes DSP-Plug-in anzeigen, um Benutzern das Festlegen von Werten zu ermöglichen, die das Verhalten des Plug-ins ändern. Benutzer können auf die Eigenschaften Seite über die Registerkarte **Plug-ins** des Dialog Felds Optionen zugreifen, indem Sie auf den Namen des DSP-Plug-Ins klicken, um es auszuwählen, und dann auf **Eigenschaften** klicken.

Der Beispielcode für den Windows Media Player-Plug-in-Assistenten stellt eine Standard Implementierung einer Eigenschaften Seite bereit, die ein einzelnes Bearbeitungsfeld enthält, das vom Benutzer einen Wert empfängt, der einen Skalierungsfaktor für das audiovolume darstellt. Wenn der Benutzer auf **anwenden** klickt, übergibt die Eigenschaften Seite diesen Wert an das Plug-in-Objekt, sodass das Plug-in den Wert ändern kann, der zum Skalieren des Volumes während der Verarbeitung verwendet wird.

## <a name="about-the-property-page-object"></a>Informationen zum Eigenschaften Seiten Objekt

Das Eigenschaften Seiten Objekt ist ein COM-Objekt, das die **IPropertyPage** -Schnittstelle implementiert. Der Beispielcode, der vom Plug-in-Assistenten generiert wird, verwendet die ATL-Implementierung von **IPropertyPage**, die in der Visual C++-Dokumentation auf MSDN dokumentiert ist. Der Code sollte zumindest Überschreibungs Implementierungen für **IPropertyPage:: OnInitDialog** bereitstellen, der das Ereignis behandelt, das beim Öffnen der Eigenschaften Seite auftritt, und **IPropertyPage:: apply**, das das Ereignis behandelt, das auftritt, wenn der Benutzer auf **anwenden** klickt. Der Plug-in-Assistent generiert Beispielcode für jeden dieser Ereignishandler. Die Beispiel Implementierung von **OnInitDialog** Ruft einen Wert aus der Registrierung ab, sodass die aktuelle Skalierungsfaktor Einstellung angezeigt werden kann. Die Beispiel Implementierung von **Apply** überprüft die Benutzereingaben, indem Sie testet, um sicherzustellen, dass Sie in einen angegebenen Bereich fällt, speichert den Wert dann in der Registrierung und übergibt dann den Wert (falls gültig) an die "DSP"-Plug-in-Eigenschaft Put-Methode mit dem Namen " **Put \_ Scale**".

Außerdem müssen Sie Code hinzufügen, um das Ereignis zu behandeln, das auftritt, wenn der Benutzer einen Wert in einem Steuerelement ändert, das Sie auf der Eigenschaften Seite angeben. Der Plug-in-Assistent implementiert beispielsweise eine Funktion mit dem Namen " **onchangescale**", die einfach die Schaltfläche " **anwenden** " aktiviert, wenn der Benutzer den Text im Bearbeitungsfeld auf der Eigenschaften Seite ändert, indem er die **SetDirty** -Methode mit dem Argument Wert **true** aufruft.

## <a name="about-the-property-page-dialog-resource"></a>Informationen über die Eigenschaften Seiten-Dialog Ressource

Die Benutzeroberfläche für die Eigenschaften Seite wird als Dialog Ressource gespeichert. Sie können das Dialogfeld "Eigenschaften Seite" auf einfache Weise in Visual Studio anzeigen und bearbeiten, indem Sie im Fenster "Projekt Arbeitsbereich" die Registerkarte " **resourceview** " auswählen und dann den **Dialog** Ordner öffnen und dann auf den Ressourcennamen der Eigenschaften Seite doppelklicken. Der Dialogfeld Ressourcen-Editor in Visual Studio stellt Ihnen die Tools zur Verfügung, die Sie zum Hinzufügen von Steuerelementen zum Dialogfeld der Eigenschaften Seite und zum Erstellen von Ereignis Handlern benötigen, die den entsprechenden Windows-Meldungen zugeordnet sind. Ausführliche Informationen zur Verwendung des Ressourcen-Editors in Visual Studio finden Sie in der Hilfe zu Visual Studio.

## <a name="about-ispecifypropertypages"></a>Informationen zu ISpecifyPropertyPages

Wenn ein DSP-Plug-in eine Eigenschaften Seite bereitstellt, muss das Plug-in die **ISpecifyPropertyPages** -Schnittstelle implementieren. Diese Schnittstelle enthält nur eine Methode: **ISpecifyPropertyPages:: GetPages**. Dies ist die Methode, die die Eigenschaften Seite dem DSP-Plug-in zuordnet. Windows Media Player ruft diese Methode auf, wenn der Benutzer die Eigenschaften Seite aufruft und dabei einen Parameter vom Typ cauuid übergibt, bei dem es sich um ein Gezähltes Array von GUIDs handelt. Die Plug-in-Beispiel Implementierung von **GetPages** füllt diese Struktur mit einer einzelnen GUID, die die Klassen-ID des Plug-in-Eigenschaften Seiten Objekts ist. Windows Media Player verwendet dann die Klassen-ID, um das Objekt der Eigenschaften Seite zu erstellen.

Sie werden feststellen, dass die Beispiel Implementierung von **GetPages** die Verwendung von **CoTaskMemAlloc** zum Zuweisen von Arbeitsspeicher für die GUID-Struktur verwendet. Es liegt in der Verantwortung des Aufrufers, in diesem Fall Windows Media Player, den Arbeitsspeicher mit " **CoTaskMemFree** " freizugeben. Ausführliche Informationen zur cauuid-Struktur finden Sie in der Platform SDK-Dokumentation.

## <a name="about-the-proxystub-dll"></a>Informationen zur Proxy-/Stub-DLL

Damit ein DSP-Plug-in in Windows Media Player 11 unter Windows Vista ausgeführt werden kann, müssen Sie eine Proxy-/Stub-DLL für benutzerdefinierte Schnittstellen bereitstellen, die zum Übermitteln von Änderungen an Einstellungen über ein Eigenschaften Seiten Dialogfeld an die Plug-in-Klasse verwendet werden. Methodenaufrufe über diese Schnittstellen müssen gemarshallt werden, wenn die Aufrufe über Prozess-oder Apartment Grenzen hinweg erfolgen. Mit der neuesten Version des Plug-in-Assistenten wird ein Beispiel für ein Proxy-/Stub-DLL-Projekt erstellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines audiodsp-Plug-ins**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




