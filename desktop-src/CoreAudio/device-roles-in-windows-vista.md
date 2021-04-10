---
description: Arbeiten mit Geräte Rollen
ms.assetid: 3b2cb1fe-0f11-4509-a6f3-513d2755cd29
title: Arbeiten mit Geräte Rollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21ea667a6974634c1f9f0657dd02c13a621641c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958143"
---
# <a name="working-with-device-roles"></a>Arbeiten mit Geräte Rollen

Die [mmdevice-API](mmdevice-api.md) unterstützt Geräte Rollen. Die [**erole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) -Enumeration definiert die Geräte Rollen, die von der mmdevice-API unterstützt werden.

> [!Note]  
> Obwohl die [mmdevice-API](mmdevice-api.md) Geräte Rollen unterstützt, implementiert die Benutzeroberfläche in Windows Vista nicht die Unterstützung für dieses Feature.

 

Eine Anwendung kann die mmdevice-API verwenden, um [Geräte Rollen](device-roles.md) über die Methoden " [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) " und " [**immnotificationclient:: ondefaultdevicechanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) " zu unterstützen. Die Benutzeroberfläche in Windows Vista unterstützt jedoch nicht die Zuweisung einzelner Rollen zu unterschiedlichen Geräten. In Windows Vista ermöglicht die Benutzeroberfläche dem Benutzer, ein Standardaudiogerät für das Rendering auszuwählen, und ein Standardaudiogerät für die Erfassung. Wenn der Benutzer ein Standard-Rendering-oder-Erfassungsgerät auswählt, weist das System alle drei Geräte Rollen (econsole, emultimedia und eCommunications) diesem Gerät zu. Anwendungen können die Rollen, die audioendpunktgeräten zugewiesen sind, nicht ändern. Das Betriebssystem ermöglicht nur dem Benutzer das Zuweisen von Geräte Rollen.

Ein Client kann sich selbst registrieren, um bei jeder Änderung bei der Zuweisung von Rollen zu audioendpunktgeräten eine Benachrichtigung von der mmdevice-API zu erhalten. Wenn eine Rolle von einem Gerät zu einem anderen verschoben wird, kann der Client auswählen, ob seine Streams weiterhin über das gleiche Gerät abgespielt (oder aufgezeichnet) werden oder ob die Streams auf ein anderes Gerät umgestellt werden. Standardmäßig werden die Streams weiterhin über das ursprüngliche Gerät abgespielt (oder aufgezeichnet). Wenn in Windows Vista die Streams auf ein anderes Gerät umgestellt werden sollen, muss der Client die Streams auf dem ursprünglichen Gerät löschen und Ersetzungs Datenströme auf dem neuen Gerät erstellen. In Windows 7 kann der Client auf neue Benachrichtigungen lauschen, um einen nahtlosen Switch zu implementieren, ohne die Wiedergabe oder die Erfassungs Sitzung zu unterbrechen. Weitere Informationen finden Sie unter [streamrouting](stream-routing.md).

Wenn Sie Windows Vista zum Testen Ihrer Anwendung verwenden möchten, können Sie eine Testumgebung einrichten, um sicherzustellen, dass sich die Anwendung erwartungsgemäß verhält, wenn der Benutzer einzelne Geräte Rollen verschiedenen Geräten zuweisen kann. Sollten Sie weitere Informationen benötigen, senden Sie eine E-Mail an uaa@microsoft.com.

## <a name="communication-devices"></a>Kommunikationsgeräte

Die Benutzeroberfläche von Windows 7 bietet die Möglichkeit, *Kommunikationsgeräte* hinzuzufügen. Mithilfe der **Sound** -Systemsteuerung können Benutzer ein Standard Kommunikationsgerät auswählen, das zum Rendern und Aufzeichnen des Audiostreams dient. Wenn ein neues Gerät mit dem Computer verbunden ist, führt das Betriebssystem standardmäßig eine automatische Rollen Erkennung durch und bestimmt, ob das Gerät für die eCommunication-Rolle geeignet ist. Wenn Sie Kommunikationsgeräte als Ziel verwenden, können Sie Anwendungen entwickeln, die Core-audioapis verwenden, um PC-Telefon-Kommunikationslösungen zu implementieren. Beispielsweise kann eine VoIP-Anwendung die Spracheingabe-und-Ausgabedaten Ströme den Standardgeräten zum Erfassen und Rendern von Endpunkten mit der eCommunications-Rolle zuweisen. Wie bei jedem anderen Datenstrom muss eine Kommunikationsanwendung einen Verweis auf den Endpunkt des kommunikationsgeräts abrufen, indem Sie [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)aufrufen. In diesem-Befehl muss die Anwendung **eCommunications** im *Role* -Parameter angeben. Die WASAPI-streamvorgänge in einem Datenstrom, der auf einem Kommunikationsgerät geöffnet ist, ähneln einem anderen Audiodatenstrom. Die Kommunikationsanwendung kann die Benutzerfreundlichkeit verbessern, indem Sie Verhalten wie das ducken durch die Verarbeitung von Benachrichtigungen vom Geräte Endpunkt implementiert. Weitere Informationen finden Sie unter [Verwenden eines kommunikationsgeräts](using-the-communication-device.md).

## <a name="automatic-device-role-detection"></a>Automatische Erkennung von Geräte Rollen

Stellen Sie sich ein Szenario vor, in dem ein Computer über ein Standardmäßiges renderinggerät, die Redner und ein Standard Erfassungsgerät, ein Mikrofon, verfügt. Der Benutzer verbindet ein USB-Headset mit dem Computer. Nachdem die entsprechenden Treiber installiert wurden, wird vom Betriebssystem versucht, eine Rolle zu ermitteln, die dem neuen Audiogerät zugewiesen werden soll.

In Windows 7 wurde das Feature zum Erkennen von Geräte Rollen erheblich verbessert, um die für Audiogeräte geeigneten geeigneten Rollen zu ermitteln. Alle Audiogeräte enthalten eine Reihe von Konfigurationseinstellungen, die vom Gerät OEM aufgefüllt werden, die dem System bei der Entscheidung helfen, wie das Gerät verwendet werden soll. Diese Einstellungen enthalten Informationen wie den physischen Speicherort des audiohandwagens, den Untertyp Jack und Erkennungsfunktionen, damit das System ermitteln kann, ob das Gerät angeschlossen ist. Wenn Sie diese Werte vom Gerät abrufen, bestimmt das Betriebssystem die Rolle, die dem Gerät zugewiesen werden soll. In diesem Szenario hat das System das USB-Headset-Gerät abgefragt, eine automatische Rollen Erkennung durchgeführt und entschieden, dass das Gerät am besten als Kommunikationsgerät geeignet ist.

Eine Anwendung kann auch Jack-Informationen mithilfe der kernaudioapis erhalten. Weitere Informationen finden Sie unter " [**iksjackdescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription) " und [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte Rollen](device-roles.md)
</dt> </dl>

 

 



