---
description: Wenn eine Anwendung eine Verbindung mit einem Hardware Gerät für die Windows-Abbild Beschaffung (WIA) herstellt, erstellt WIA eine Elementstruktur (eine hierarchische Struktur von iwiaitem-oder IWiaItem2-Schnittstellen), die das Gerät und seine Bilder, Ordner und Scanvorgänge darstellt.
ms.assetid: 2a7bcfd4-4075-48a4-9eff-5210b9a635e3
title: Auswählen eines Geräts (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a2eab41016397f6505e60efcbf78d1fdf82499
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862671"
---
# <a name="selecting-a-device-wia"></a>Auswählen eines Geräts (WIA)

Wenn eine Anwendung eine Verbindung mit einem Hardware Gerät für die Windows-Abbild Beschaffung (WIA) herstellt, erstellt WIA eine Elementstruktur (eine hierarchische Struktur von [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -oder [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstellen), die das Gerät und seine Bilder, Ordner und Scanvorgänge darstellt. Eine Anwendung kann ein Gerät ohne Benutzereingabe auswählen und eine Verbindung mit ihm herstellen, oder es kann ein Dialogfeld angezeigt werden, in dem ein Benutzer ein Gerät auswählen kann.

-   [Auswählen eines Geräts ohne die Benutzeroberfläche](#selecting-a-device-without-the-ui)
-   [Auswählen eines Geräts mithilfe der Benutzeroberfläche](#selecting-a-device-with-the-ui)

## <a name="selecting-a-device-without-the-ui"></a>Auswählen eines Geräts ohne die Benutzeroberfläche

Führen Sie die folgenden Schritte aus, um ein WIA-Hardware Gerät auszuwählen und eine Verbindung mit ihm herzustellen.

-   Rufen Sie [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um einen Zeiger auf die [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) -oder [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) -Schnittstelle abzurufen.
-   Verwenden Sie die [**iwiadevmgr:: enumdeviceinfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) -Methode der [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) -oder [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) -Schnittstelle, um einen Zeiger auf die [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) -Schnittstelle zu erhalten. Anweisungen zum Auflisten von Geräten finden Sie unter Auflisten von [System Geräten](-wia-enumerating-system-devices.md).
-   Verwenden Sie [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) Interface, um [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Schnittstellen Zeiger für jedes aufgelistete WIA-Gerät abzurufen.
-   Verwenden Sie [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) Interface, um die Geräte Informations Eigenschaften jedes Geräts zu überprüfen und die WIA \_ DIP \_ dev-ID- \_ Eigenschaft vom gewünschten Gerät zu speichern.
-   Verwenden Sie die DeviceID-Eigenschaft mit der [**iwiadevmgr:: anatedevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) -Methode in der [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) -oder [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) -Schnittstelle, um ein WIA-Geräte Objekt zu erstellen. Die **iwiadevmgr:: deatedevice** -Methode stellt der Anwendung den Zeiger auf die [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -oder [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des Stamm Elements des angegebenen Geräts bereit.

Ein Beispiel dafür, wie Sie dies in einer Anwendung durchführen können, finden Sie im Abschnitt [Erstellen eines Geräts](-wia-creating-a-device.md) im Tutorial dieses Handbuchs.

## <a name="selecting-a-device-with-the-ui"></a>Auswählen eines Geräts mithilfe der Benutzeroberfläche

Nach dem Abrufen eines Zeigers auf [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)kann eine Anwendung einem Benutzer ermöglichen, ein Gerät auszuwählen, indem er die restlichen Schritte überspringt und [**iwiadevmgr:: SelectDeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlg)anruft. **Iwiadevmgr:: selectde vicedlg** zeigt ein Dialogfeld an, in dem der Benutzer ein WIA-Gerät auswählen kann.

Es wird empfohlen, dass Anwendungen die Geräte-und Abbild Auswahl über ein Menü Element namens **von Scanner** im Menü **Datei** verfügbar machen.

 

 
