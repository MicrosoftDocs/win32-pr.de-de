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
# <a name="device-input-and-output-control-ioctl"></a><span data-ttu-id="982b6-103">Geräte Eingabe-und-Ausgabe Steuerung (IOCTL)</span><span class="sxs-lookup"><span data-stu-id="982b6-103">Device Input and Output Control (IOCTL)</span></span>

<span data-ttu-id="982b6-104">Die Funktion [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) bietet eine ioctl-Schnittstelle (Device Input and Output Control), über die eine Anwendung direkt mit einem Gerätetreiber kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="982b6-104">The [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function provides a device input and output control (IOCTL) interface through which an application can communicate directly with a device driver.</span></span> <span data-ttu-id="982b6-105">Die Funktion **DeviceIoControl** ist eine allgemeine Schnittstelle, mit der Steuerungs Codes an verschiedene Geräte gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="982b6-105">The **DeviceIoControl** function is a general-purpose interface that can send control codes to a variety of devices.</span></span> <span data-ttu-id="982b6-106">Jeder Steuerelement Code stellt einen Vorgang dar, der vom Treiber durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="982b6-106">Each control code represents an operation for the driver to perform.</span></span> <span data-ttu-id="982b6-107">Beispielsweise kann ein Steuerungs Code einen Gerätetreiber bitten, Informationen zum entsprechenden Gerät zurückzugeben, oder den Treiber anweisen, eine Aktion auf dem Gerät auszuführen, z. b. das Formatieren eines Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="982b6-107">For example, a control code can ask a device driver to return information about the corresponding device, or direct the driver to carry out an action on the device, such as formatting a disk.</span></span>

<span data-ttu-id="982b6-108">In den SDK-Header Dateien sind einige Standard Kontrollcodes definiert.</span><span class="sxs-lookup"><span data-stu-id="982b6-108">A number of standard control codes are defined in the SDK header files.</span></span> <span data-ttu-id="982b6-109">Außerdem können Gerätetreiber eigene gerätespezifische Steuerungs Codes definieren.</span><span class="sxs-lookup"><span data-stu-id="982b6-109">In addition, device drivers can define their own device-specific control codes.</span></span> <span data-ttu-id="982b6-110">Eine Liste der Standard Steuercodes, die in der SDK-Dokumentation enthalten sind, finden Sie im Abschnitt "Hinweise" von [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).</span><span class="sxs-lookup"><span data-stu-id="982b6-110">For a list of standard control codes included in the SDK documentation, see the Remarks section of [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).</span></span>

<span data-ttu-id="982b6-111">Die Typen von Steuerungs Codes, die Sie angeben können, hängen vom Gerät, auf das zugegriffen wird, und von der Plattform ab, auf der die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="982b6-111">The types of control codes you can specify depend on the device being accessed and the platform on which your application is running.</span></span> <span data-ttu-id="982b6-112">Anwendungen können die Standard Steuercodes oder gerätespezifischen Steuerungs Codes verwenden, um direkte Eingabe-und Ausgabe Vorgänge auf einem Diskettenlaufwerk, einem Festplattenlaufwerk, einem Bandlaufwerk oder einem CD-ROM-Laufwerk auszuführen.</span><span class="sxs-lookup"><span data-stu-id="982b6-112">Applications can use the standard control codes or device-specific control codes to perform direct input and output operations on a floppy disk drive, hard disk drive, tape drive, or CD-ROM drive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="982b6-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="982b6-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="982b6-114">Aufrufen von DeviceIoControl</span><span class="sxs-lookup"><span data-stu-id="982b6-114">Calling DeviceIoControl</span></span>](calling-deviceiocontrol.md)
</dt> </dl>

 

 
