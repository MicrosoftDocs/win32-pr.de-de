---
description: Die folgenden Funktionen werden mit dem Output Protection Manager (OPM) verwendet.
ms.assetid: 7ecde6ae-56fd-451b-bebb-224c6801be05
title: OPM-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b4ef210ace3f7f179b59980cedb962a5bee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345816"
---
# <a name="opm-functions"></a>OPM-Funktionen

Die folgenden Funktionen werden mit dem [Output Protection Manager](output-protection-manager.md) (OPM) verwendet.



| Funktion                                                                                             | BESCHREIBUNG                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Opmgetvideooutputfortarget**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputfortarget)                                     | Gibt ein Videoausgabe Objekt für das VidPN-Ziel auf dem angegebenen Adapter zurück.                                                          |
| [**Opmgetvideooutputsfromhmonitor**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)                             | Erstellt ein OPM-Objekt (Output Protection Manager) für jeden physischen Monitor, der einem bestimmten **Hmonitor** -Handle zugeordnet ist. |
| [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) | Erstellt ein OPM-Objekt für jeden physischen Monitor, der einem bestimmten Direct3D-Gerät zugeordnet ist.                                 |



 

Die folgenden Funktionen werden von OPM verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen. Anwendungen sollten diese Funktionen nicht aufzurufen.

-   [**Konfiguration von reopmprotectedoutput**](configureopmprotectedoutput.md)
-   [**"Kreateopmprotectedoutputs"**](createopmprotectedoutputs.md)
-   [**Destroyopmprotectedoutput**](destroyopmprotectedoutput.md)
-   [**Von GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate)
-   [**Getcertifialisiesize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize)
-   [**Getcoppcompatibleopminformation**](getcoppcompatibleopminformation.md)
-   [**Getopminformation**](getopminformation.md)
-   [**Getopmrandomnumber**](getopmrandomnumber.md)
-   [**Getvorschlags stedopmprotectedoutputarraysize**](getsuggestedopmprotectedoutputarraysize.md)
-   [**"Setup" für "Setup keyandsequencenumbers"**](setopmsigningkeyandsequencenumbers.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[OPM-Programmier Referenz](opm-programming-reference.md)
</dt> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> </dl>

 

 



