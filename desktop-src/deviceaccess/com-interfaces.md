---
title: COM-Schnittstellen – Gerätezugriff
description: Component Object Model (COM)-Schnittstellen im Gerätezugriffs-API.
ms.assetid: 96F532B7-5CF9-4341-932B-7F8BEDA9551F
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 22447151b944a2ac5515222eebd528fed11e2479d8a8c4db59e2da46dd07a130
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793385"
---
# <a name="com-interfaces---device-access"></a>COM-Schnittstellen – Gerätezugriff

Component Object Model (COM)-Schnittstellen im Gerätezugriffs-API.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|---|---|
| [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)<br/> | Die [**ICreateDeviceAccessAsync-Schnittstelle**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) wird von einem Aufruf von CreateDeviceAccessInstance zurückgegeben. Sie ermöglicht es dem Aufrufer, den Vorgang der Bindung an eine Instanz eines Geräts zu steuern, um eine andere Schnittstelle abzurufen, die für die Interaktion mit diesem Gerät verwendet werden kann.<br/> |
| [**IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol)<br/> | Sendet einen Steuerungscode an einen Gerätetreiber. Diese Aktion bewirkt, dass das Gerät den entsprechenden Vorgang ausführt. <br/> |
| [**IDeviceRequestCompletionCallback**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)<br/> | Stellt eine Methode bereit, um den Abschluss von Aufrufen der [**DeviceIoControlAsync-Methode**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync)zu verarbeiten.<br/> |

## <a name="related-topics"></a>Zugehörige Themen

Beispiel für [benutzerdefinierten Treiberzugriff,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Hardware Dev Center](/windows-hardware/drivers/)
