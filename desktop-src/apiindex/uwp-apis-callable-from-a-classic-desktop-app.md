---
description: Die allgemeine Regel ist, dass eine Desktop-App eine Windows-Runtime (WinRT)-API aufgerufen werden kann. Einige APIs, einschließlich der XAML-UI-APIs, erfordern jedoch, dass die aufrufenden App über eine Paket Identität verfügt.
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: WinRT-APIs, die von einer Desktop-App aufgerufen werden können
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9083fbfb16391c626f49b79176fed7a81068c028
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2020
ms.locfileid: "104039833"
---
# <a name="calling-winrt-apis-from-a-desktop-app"></a>Aufrufen von WinRT-APIs aus einer Desktop-App

Die allgemeine Regel ist, dass eine Desktop-App eine WinRT-API aufgerufen werden kann. Einige APIs, einschließlich der XAML-UI-APIs, erfordern jedoch, dass die aufrufenden App über eine Paket Identität verfügt. UWP-apps verfügen über ein klar definiertes App-Modell, und Sie verfügen über eine Paket Identität. Die anderen Typen von Desktop-apps haben weder ein klar definiertes App-Modell noch eine Paket Identität. Wenn also eine API eine Paket Identität erfordert, kann Sie von einer WPF-, Windows Forms-oder Win32-app nur aufgerufen werden, wenn die APP [in einem msix-Paket verpackt ist](/windows/msix/desktop/desktop-to-uwp-root).

## <a name="the-dualapipartition-attribute"></a>Das dualapipartition-Attribut

Dies ist der Prozess, der immer dann befolgt werden soll, wenn ein bestimmter WinRT-Vorgang von Ihrer Desktop-App aus aufgerufen werden soll. Durch diesen Vorgang wird die Frage beantwortet, ob die API von einer Desktop-App aufgerufen werden darf. Besuchen Sie zunächst die [Windows-API-Referenz für Windows-Runtime-apps](/uwp/), suchen Sie das Referenz Thema für die Klasse oder die Member-API, an der Sie interessiert sind, und überprüfen Sie, ob das [**dualapipartition**](/uwp/api/Windows.Foundation.Metadata.DualApiPartitionAttribute) -Attribut im Abschnitt Attribute aufgeführt ist.

## <a name="if-the-dualapipartition-attribute-is-listed"></a>Wenn das dualapipartition-Attribut aufgelistet ist

Wenn das Attribut "dualapipartition" aufgeführt wird, benötigt die API nicht, dass die aufrufende App über eine Paket Identität verfügt, und die API kann von jeder Desktop-App aus aufgerufen werden. [**Windows. Devices. geoloation. GeoLocator**](/uwp/api/Windows.Devices.Geolocation.Geolocator) ist ein Beispiel. eine APP muss nicht eindeutig identifiziert werden, um Standort Aufgaben ausführen zu können.

## <a name="if-the-dualapipartition-attribute-is-not-listed"></a>Wenn das dualapipartition-Attribut nicht aufgeführt ist

Wenn das Attribut "dualapipartition" nicht aufgeführt ist, benötigt die API die aufrufenden App für eine Paket Identität. Daher ist eine WPF-, Windows Forms-oder Win32-APP nicht berechtigt, die API aufzurufen, es sei denn, die APP wurde in eine UWP-App konvertiert. [**Windows. UI. XAML. Controls. Button**](/uwp/api/Windows.UI.Xaml.Controls.Button) ist ein Beispiel.
