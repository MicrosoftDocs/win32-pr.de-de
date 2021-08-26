---
description: Die Windows Image Acquisition(WIA)-APIs geben ihren Abschlussstatus in einem HRESULT-Rückgabewert zurück.
ms.assetid: 4f3b4292-7aad-4a0a-9cd7-ef8438e57ab3
title: WIA-Fehlerinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce8181cb4d3f578fa9322ecaa81d588423bb403be3b38a76c2dbac17a19fe010
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056960"
---
# <a name="wia-error-information"></a>WIA-Fehlerinformationen

Die Windows Image Acquisition(WIA)-APIs geben ihren Abschlussstatus in einem HRESULT-Rückgabewert zurück. Anwendungen überprüfen diese Rückgabewerte anhand der FACILITY \_ WIA-Konstante, um zu ermitteln, ob für den Fehler ein Benutzereingriff erforderlich ist, um diesen zu löschen, z. B. einen eingesäten Papierpfad, und melden sie dem Benutzer. Darüber hinaus werden alle Fehler auf Treiberebene ausführlich im Ereignisprotokoll protokolliert, indem vom Minitreiber des Geräts bereitgestellte Fehlerzeichenfolgen verwendet werden. Eine Liste der WIA-spezifischen Fehlercodes finden Sie unter [Fehlercodes.](-wia-error-codes.md)

 

 



