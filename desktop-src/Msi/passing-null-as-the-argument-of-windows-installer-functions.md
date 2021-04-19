---
description: Windows Installer Funktionen, die Daten in einem vom Benutzer bereitgestellten –-Speicherort zurückgeben, dürfen nicht mit NULL als Wert für den Zeiger aufgerufen werden.
ms.assetid: f566c4a4-b90c-4d73-9d7f-f5b836630636
title: Übergeben von NULL an Windows Installer Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb09ceb3982695792614a3c226af9ab276aa3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348274"
---
# <a name="passing-null-as-the-argument-of-windows-installer-functions"></a>Übergeben von NULL als Argument Windows Installer Funktionen

Windows Installer Funktionen, die Daten in einem vom Benutzer bereitgestellten –-Speicherort zurückgeben, dürfen nicht mit NULL als Wert für den Zeiger aufgerufen werden. Diese Funktionen geben eine Zeichenfolge oder Rückgabe Daten als ganzzahlige Zeiger zurück, geben jedoch inkonsistente Werte zurück, wenn NULL als Wert für das Output-Argument übergeben wird.

Übergeben Sie NULL nicht als Wert des Output-Arguments für eine der folgenden Funktionen:

[**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)

[**Msirecordgetstring**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)

[**Msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)

[**Msigetsourcepath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)

[**Msigettargetpath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[**Msiviewgeterror**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)

[**Msisummaryinfogetproperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)

[**Msievaluatecondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)

[**Msigetfeaturecost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)

[**Msigetfeaturecost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[**Msigetfeaturevalidstates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)

 

 



