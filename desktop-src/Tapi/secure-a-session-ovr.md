---
description: Wenn eine Anwendung keine Störungen durch externe Ereignisse für eine Sitzung von TAPI oder dem Dienstanbieter möchte, sollte sie den Aufruf sichern.
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: Sichern einer Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64ee16dc0854c6502f1347a3aa676e709920555ad91a02190db001bd80b34824
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080460"
---
# <a name="secure-a-session"></a>Sichern einer Sitzung

Wenn eine Anwendung keine Störungen durch externe Ereignisse für eine Sitzung von TAPI oder dem Dienstanbieter möchte, sollte sie den Aufruf sichern. In einer analogen Umgebung können Anrufwartetons beispielsweise ein Fax oder eine Modemsitzung beim ursprünglichen Anruf zerstören.

Eine Anwendung kann einen Aufruf sichern, wenn der Aufruf erfolgt oder der Aufruf bereits vorhanden ist.

Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.

**TAPI 2.x:** Siehe [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).

**TAPI 3.x:** Weitere Informationen [**finden Sie unter ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).

 

 
