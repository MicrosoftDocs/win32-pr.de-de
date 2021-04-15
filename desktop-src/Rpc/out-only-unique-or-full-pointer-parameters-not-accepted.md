---
title: Out-Only eindeutige oder vollständige Zeiger Parameter nicht akzeptiert.
description: Eindeutige oder vollständige Zeiger, bei denen es sich nicht um \ out handelt, werden vom Mittelwert Compiler nicht akzeptiert. Diese Spezifikationen bewirken, dass der Mittell-Compiler eine Fehlermeldung generiert.
ms.assetid: 0477980e-d76e-452f-9ab1-71a8ed8642d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b21baa370c1b68fb3c708a8fdb21115686646f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516976"
---
# <a name="out-only-unique-or-full-pointer-parameters-not-accepted"></a>Out-Only eindeutige oder vollständige Zeiger Parameter nicht akzeptiert.

Eindeutige oder vollständige Zeiger, die nicht als veraltet gelten, \[ [](/windows/desktop/Midl/out-idl) \] werden vom Mittelwert Compiler nicht akzeptiert. Diese Spezifikationen bewirken, dass der Mittell-Compiler eine Fehlermeldung generiert.

Der automatisch generierte Serverstub muss Speicher für den Zeiger Referenten zuweisen, damit die Serveranwendung Daten in diesem Speicherbereich speichern kann. Gemäß der Definition eines reinen **\[ out \]**-Parameters werden keine Informationen über den-Parameter vom Client an den Server übertragen. Im Fall eines eindeutigen Zeigers, der den Wert NULL annehmen kann, verfügt der Serverstub nicht über genügend Informationen zum korrekten Duplizieren des eindeutigen Zeigers im Adressraum des Servers, und der Stub hat keine Informationen darüber, ob der Zeiger auf eine gültige Adresse zeigen soll oder ob er auf NULL festgelegt werden soll. Daher ist diese Kombination nicht zulässig.

Anstatt \[ **out**, [Unique](/windows/desktop/Midl/unique) \] oder \[ **out**, [ptr](/windows/desktop/Midl/ptr) \] -Zeiger, use \[ **in**, **out**, **Unique** \] oder \[ **in**, **out**, **ptr** - \] Zeiger, oder verwenden Sie eine andere Dereferenzierungsebene, z. b. einen Verweis Zeiger, der auf den gültigen eindeutigen oder vollständigen Zeiger zeigt.

 

 