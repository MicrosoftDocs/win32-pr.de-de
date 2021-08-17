---
title: Out-Only eindeutige oder vollständige Zeigerparameter nicht akzeptiert
description: Eindeutige oder vollständige Zeiger, die \out\ -only sind, werden vom MIDL-Compiler nicht akzeptiert. Solche Spezifikationen führen dazu, dass der MIDL-Compiler eine Fehlermeldung generiert.
ms.assetid: 0477980e-d76e-452f-9ab1-71a8ed8642d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9511c21045892eb7a5b3230d8f0180578b489b06b5b5402fb0b11f6a3ff31a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927569"
---
# <a name="out-only-unique-or-full-pointer-parameters-not-accepted"></a>Out-Only eindeutige oder vollständige Zeigerparameter nicht akzeptiert

Eindeutige oder vollständige Zeiger, die \[ [nur out](/windows/desktop/Midl/out-idl) \] sind, werden vom MIDL-Compiler nicht akzeptiert. Solche Spezifikationen führen dazu, dass der MIDL-Compiler eine Fehlermeldung generiert.

Der automatisch generierte Serverstub muss Arbeitsspeicher für den Zeigerreferenz zuweisen, damit die Serveranwendung Daten in diesem Speicherbereich speichern kann. Gemäß der Definition eines **\[ \]** out-only-Parameters werden keine Informationen über den Parameter vom Client an den Server übertragen. Im Fall eines eindeutigen Zeigers, der den Wert NULL übernehmen kann, verfügt der Serverstub nicht über genügend Informationen, um den eindeutigen Zeiger im Adressraum des Servers ordnungsgemäß zu duplizieren, und der Stub verfügt auch nicht über Informationen darüber, ob der Zeiger auf eine gültige Adresse zeigen oder auf NULL festgelegt werden soll. Daher ist diese Kombination nicht zulässig.

Verwenden Sie anstelle von out , unique oder \[  [](/windows/desktop/Midl/unique) \] \[ **out**, [ptr-Zeigern](/windows/desktop/Midl/ptr) in , out , unique oder \] \[    \] \[ **in**, **out**, **ptr-Zeigern,** \] oder verwenden Sie eine andere Dereferenzierungsebene, z. B. einen Verweiszeiger, der auf den gültigen eindeutigen oder vollständigen Zeiger zeigt.

 

 