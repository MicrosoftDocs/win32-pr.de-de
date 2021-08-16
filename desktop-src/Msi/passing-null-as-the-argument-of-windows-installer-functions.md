---
description: Windows Installerfunktionen, die Daten an einem vom Benutzer bereitgestellten Speicherort zurückgeben, sollten nicht mit NULL als Wert für den Zeiger aufgerufen werden.
ms.assetid: f566c4a4-b90c-4d73-9d7f-f5b836630636
title: Übergeben von NULL an Windows Installer-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6964716479d7e64cc9aa70d7e49acc8fe78dd3343298826e011f6d72b4df1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627663"
---
# <a name="passing-null-as-the-argument-of-windows-installer-functions"></a>Übergeben von NULL als Argument Windows Installer-Funktionen

Windows Installerfunktionen, die Daten an einem vom Benutzer bereitgestellten Speicherort zurückgeben, sollten nicht mit NULL als Wert für den Zeiger aufgerufen werden. Diese Funktionen geben eine Zeichenfolge oder Daten als Ganzzahlzeiger zurück, geben jedoch inkonsistente Werte zurück, wenn NULL als Wert für das Ausgabeargument übergeben wird.

Übergeben Sie null nicht als Wert des Ausgabearguments für eine der folgenden Funktionen:

[**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)

[**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)

[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)

[**MsiGetSourcePath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)

[**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)

[**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)

[**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)

[**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)

[**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)

 

 



