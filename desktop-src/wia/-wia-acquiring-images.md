---
description: Nachdem ein Image ausgewählt wurde, verwendet eine Anwendung die iwiadatatransfer-Schnittstelle (für Anwendungen, die unter Windows XP oder früher ausgeführt werden) oder die iwiatransfer-Schnittstelle (für Anwendungen, die in Windows Vista oder höher ausgeführt werden), um Abbild Daten von Bildverarbeitungsgeräten zu übertragen. Weitere Informationen finden Sie unter Übertragen von Bilddaten in WIA 1,0 oder übertragen von Bilddaten in WIA 2,0.
ms.assetid: cf76e526-d63b-4ee5-ba3c-871f2051a82c
title: Abrufen von Images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d062cb370327311ad0c7d4f883344c05bb776f6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350241"
---
# <a name="acquiring-images"></a>Abrufen von Images

Nachdem ein Image ausgewählt wurde, verwendet eine Anwendung die [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) -Schnittstelle (für Anwendungen, die unter Windows XP oder früher ausgeführt werden) oder die [**iwiatransfer**](-wia-iwiatransfer.md) -Schnittstelle (für Anwendungen, die in Windows Vista oder höher ausgeführt werden), um Abbild Daten von Bildverarbeitungsgeräten zu übertragen. Weitere Informationen finden Sie unter über [tragen von Bilddaten in WIA 1,0](-wia-transferring-image-data.md) oder über [tragen von Bilddaten in WIA 2,0](-wia-transferring-image-data-in-wia2.md) .

Nachdem ein Gerät ausgewählt wurde, verwendet eine Anwendung die [**iwiaitem::D evicedlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) -Methode der [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -oder [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des Geräts (das Stamm Element), um ein Abbild von einem angegebenen Windows-Abbild Erfassungsgerät (WIA) auszuwählen. Die [**iwiadevmgr:: getimagedlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) -Methode zeigt ein Dialogfeld an, in dem ein Benutzer ein Bild von einem angegebenen Gerät auswählen und das Bild auf einen vom Benutzer ausgewählten Dateinamen übertragen kann. Außerdem kann der Benutzer ggf. ein Gerät angeben. Weitere Informationen finden Sie unter [Auswählen eines Geräts](-wia-selecting-a-device.md) .

Beachten Sie, dass es nicht erforderlich ist, dass ein Benutzer ein Bild mithilfe der obigen Methode auswählt. Eine Anwendung kann einen Zeiger auf ein Bildelement direkt aus der Elementstruktur eines Geräts abrufen. Anweisungen finden Sie unter [Navigieren in einer Element](-wia-navigating-an-item-tree.md)Struktur.

Nachdem das WIA-Element ausgewählt wurde, das das gewünschte Image darstellt, fragt eine Anwendung, die unter Windows XP oder früher ausgeführt wird, die [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Schnittstelle dieses Elements nach einem Zeiger auf die [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) -Schnittstelle ab. Eine Anwendung, die unter Windows Vista oder höher ausgeführt wird, fragt die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle nach einem Zeiger auf die [**iwiatransfer**](-wia-iwiatransfer.md) -Schnittstelle ab.

Die Anwendung kann dann die Methoden der [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) -Schnittstelle (oder [**iwiatransfer**](-wia-iwiatransfer.md)) verwenden, um die Bilddaten an die Anwendung zu übertragen.

Wenn das Abbild Erstellungs Gerät ein Scanner ist, löst [**iwiadatatransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata)oder andere Methoden der [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) -Schnittstelle einen Scanvorgang aus und überträgt dann die resultierenden Bilddaten. Wenn das Gerät eine Kamera ist, werden die Bilddaten einfach von der Kamera an die Anwendung übertragen.

 

 



