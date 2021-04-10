---
description: Die Funktion DeviceIoControl bietet eine ioctl-Schnittstelle (Device Input and Output Control), über die eine Anwendung direkt mit einem Gerätetreiber kommunizieren kann.
ms.assetid: 2dffd86a-162c-4e09-bfa1-73b87522741a
title: Geräte Eingabe-und-Ausgabe Steuerung (IOCTL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2bb2ee26c63c2aad02d8e8d167ff12383fc6b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861487"
---
# <a name="device-input-and-output-control-ioctl"></a>Geräte Eingabe-und-Ausgabe Steuerung (IOCTL)

Die Funktion [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) bietet eine ioctl-Schnittstelle (Device Input and Output Control), über die eine Anwendung direkt mit einem Gerätetreiber kommunizieren kann. Die Funktion **DeviceIoControl** ist eine allgemeine Schnittstelle, mit der Steuerungs Codes an verschiedene Geräte gesendet werden können. Jeder Steuerelement Code stellt einen Vorgang dar, der vom Treiber durchgeführt werden soll. Beispielsweise kann ein Steuerungs Code einen Gerätetreiber bitten, Informationen zum entsprechenden Gerät zurückzugeben, oder den Treiber anweisen, eine Aktion auf dem Gerät auszuführen, z. b. das Formatieren eines Datenträgers.

In den SDK-Header Dateien sind einige Standard Kontrollcodes definiert. Außerdem können Gerätetreiber eigene gerätespezifische Steuerungs Codes definieren. Eine Liste der Standard Steuercodes, die in der SDK-Dokumentation enthalten sind, finden Sie im Abschnitt "Hinweise" von [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).

Die Typen von Steuerungs Codes, die Sie angeben können, hängen vom Gerät, auf das zugegriffen wird, und von der Plattform ab, auf der die Anwendung ausgeführt wird. Anwendungen können die Standard Steuercodes oder gerätespezifischen Steuerungs Codes verwenden, um direkte Eingabe-und Ausgabe Vorgänge auf einem Diskettenlaufwerk, einem Festplattenlaufwerk, einem Bandlaufwerk oder einem CD-ROM-Laufwerk auszuführen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufrufen von DeviceIoControl](calling-deviceiocontrol.md)
</dt> </dl>

 

 
