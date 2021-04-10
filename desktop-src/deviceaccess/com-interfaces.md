---
title: 'COM-Schnittstellen: Gerätezugriff'
description: Component Object Model (com)-Schnittstellen in der Geräte Zugriffs-API.
ms.assetid: 96F532B7-5CF9-4341-932B-7F8BEDA9551F
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 07abbfd15f8383bbbd9cd9d1f5fc4c9fb1f42b9e
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039803"
---
# <a name="com-interfaces---device-access"></a>COM-Schnittstellen: Gerätezugriff

Component Object Model (com)-Schnittstellen in der Geräte Zugriffs-API.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|---|---|
| [**Ikreatedeviceaccessasync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)<br/> | Die [**ikreatedeviceaccessasync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) -Schnittstelle wird von einem aufzurufenden aufrufswert zurückgegeben. Sie ermöglicht es dem Aufrufer, den Vorgang der Bindung an eine Instanz eines Geräts zu steuern, um eine andere Schnittstelle abzurufen, die für die Interaktion mit dem Gerät verwendet werden kann.<br/> |
| [**Ideviceiocontrol**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol)<br/> | Sendet einen Steuerungs Code an einen Gerätetreiber. Diese Aktion bewirkt, dass das Gerät den entsprechenden Vorgang ausführt. <br/> |
| [**Idevicerequestcompletioncallback**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)<br/> | Stellt eine Methode bereit, mit der der Abschluss von Aufrufen der [**deviceiocontrolasync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync)-Methode behandelt werden soll.<br/> |

## <a name="related-topics"></a>Zugehörige Themen

[Beispiel für benutzerdefinierten Treiber Zugriff](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware dev Center](/windows-hardware/drivers/)
