---
title: WM/wmshadowfilesourcedrmtype (Windows Media Format 11 SDK)
description: Das Attribut WM/wmshadowfilesourcedrmtype enthält den Typ von Rights Management, der zum Schutz der ursprünglichen Datei verwendet wird, von der die ASF-Datei abgeleitet ist.
ms.assetid: 58e7a383-6e80-42fc-bc75-5920dbe67a40
keywords:
- WM/wmshadowfilesourcedrmtype Windows Media-Format
topic_type:
- apiref
api_name:
- WM/WMShadowFileSourceDRMType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f33d961e8cd3645e4949980d91fe4de79119f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039992"
---
# <a name="wmwmshadowfilesourcedrmtype-windows-media-format-11-sdk"></a>WM/wmshadowfilesourcedrmtype (Windows Media Format 11 SDK)

Das Attribut **WM/wmshadowfilesourcedrmtype** enthält den Typ von Rights Management, der zum Schutz der ursprünglichen Datei verwendet wird, von der die ASF-Datei abgeleitet ist.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmwmshadowfilesourcedrmtype

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Inhalte, die sich in einem anderen Dateiformat als "ASF" befinden und durch eine Art von Rights Management geschützt sind, können durch einen Prozess namens "Lizenz Import" in eine Windows Media-Datei konvertiert werden, die von Windows Media DRM geschützt wird. Eine solche ASF-Datei sollte dieses Attribut sowie WM/wmshadowfilesourcefiletype enthalten, um zu verfolgen, woher der Inhalt stammt.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




