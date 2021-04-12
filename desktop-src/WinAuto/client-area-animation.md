---
title: Animations Parameter für Client Bereich
description: Das clientbereichsanimations-Flag gibt an, ob der Benutzer Animationen in Benutzeroberflächen Elementen deaktivieren möchte.
ms.assetid: 4a3ec9da-d5ae-4cd9-8222-f02143895ce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c62e25fdb08022d53cbe9e818a0a1089988cd6a6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209346"
---
# <a name="client-area-animation-parameter"></a>Animations Parameter für Client Bereich

Der Animations Parameter für den Client Bereich gibt an, ob der Benutzer Animationen in Benutzeroberflächen Elementen deaktivieren möchte. Anzeigen von Features wie blinken, blinken, Flimmern und Verschieben von Inhalten kann bei Benutzern mit Foto sensibler Epilepsie zu Angriffen führen. Mit diesem Parameter können Sie all diese Animationen aktivieren oder deaktivieren.

Anwendungen verwenden die **SPI-Flags \_ getclientareaanimation** und **SPI \_ setclientareaanimation** mit der [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion, um Client Bereichs Animationen ein-oder auszuschalten.

 

 