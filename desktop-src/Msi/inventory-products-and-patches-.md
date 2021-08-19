---
description: 'Benutzer und Anwendungen mit Administratorrechten können Windows Installer-Funktionen verwenden, um die auf dem System installierten Windows Installer-Anwendungen, -Features, -Komponenten und -Patches zu inventarisieren. Ab Windows Installer&\# 160;3.0 können Benutzer und Anwendungen mit Administratorrechten die anwendungen, Features, Komponenten und Patches des Windows Installers aufzählen, die von allen Benutzern auf dem System installiert wurden. Administratoren und Anwendungen können Informationen zu einem Produkt oder Patch für einen bestimmten Benutzer oder alle Benutzer im System abrufen. Anwendungen können den Funktions- oder Komponentenzustand für einen bestimmten Benutzer abrufen. Die inventurfunktionen, die ab Windows Installer&\# 160;3.0 verfügbar sind, können den Bereich der Elemente einschränken, die nach Installationskontext und Benutzerkontext gefunden werden. Es gibt drei mögliche Installationskontexte: pro Benutzer, pro Computer und pro Benutzer verwaltet. Der Benutzerkontext kann ein bestimmter Benutzer oder alle Benutzer im System sein. Die Versionen der Windows Installer-Inventurfunktionen vor Windows Installer&\# 160;3.0 können nur Elemente aufzählen, die auf dem System im Computerkontext oder im Benutzerkontext des aktuellen Benutzers installiert sind. Diese Einschränkung verhindert eine vollständige Inventur aller Windows Installer-Produkte und -Patches, die von anderen Benutzern als dem aktuellen Benutzer im System installiert werden. Enumerating ProductsEnumerating PatchesObtaining Product InformationObtaining Patch InformationObtaining Component State InformationObtaining Feature State Information'
ms.assetid: ef95c3c8-b4c8-4305-8aa2-07ec74b3121b
title: Verwenden Windows Installers zum Inventarisieren von Produkten und Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9406d0984e58efdb8344fbf8974234690e3a6aaeb1cc697b5a76e6af940554e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013228"
---
# <a name="using-windows-installer-to-inventory-products-and-patches"></a>Verwenden Windows Installers zum Inventarisieren von Produkten und Patches

Benutzer und Anwendungen mit Administratorrechten können Windows Installer-Funktionen verwenden, um die auf dem System installierten Windows Installer-Anwendungen, -Features, -Komponenten und -Patches zu inventarisieren.

Ab Windows Installer 3.0 können Benutzer und Anwendungen mit Administratorrechten die Windows Installer-Anwendungen, -Features, -Komponenten und -Patches aufzählen, die von allen Benutzern auf dem System installiert werden. Administratoren und Anwendungen können Informationen zu einem Produkt oder Patch für einen bestimmten Benutzer oder alle Benutzer im System abrufen. Anwendungen können den Funktions- oder Komponentenzustand für einen bestimmten Benutzer abrufen.

Die mit Windows Installer 3.0 verfügbaren Inventurfunktionen können den Bereich der Elemente einschränken, die nach Installationskontext und Benutzerkontext gefunden werden. Es gibt drei mögliche Installationskontexte: pro Benutzer, pro Computer und pro Benutzer verwaltet. Der Benutzerkontext kann ein bestimmter Benutzer oder alle Benutzer im System sein.

Die Versionen der Windows Installer-Inventurfunktionen vor Windows Installer 3.0 können nur Elemente aufzählen, die auf dem System im Computerkontext oder im Benutzerkontext des aktuellen Benutzers installiert sind. Diese Einschränkung verhindert eine vollständige Inventur aller Windows Installer-Produkte und -Patches, die von anderen Benutzern als dem aktuellen Benutzer im System installiert werden.

-   [Aufzählen von Produkten](#enumerating-products)
-   [Aufzählen von Patches](#enumerating-patches)
-   [Abrufen von Produktinformationen](#obtaining-product-information)
-   [Abrufen von Patchinformationen](#obtaining-patch-information)
-   [Abrufen von Komponentenzustandsinformationen](#obtaining-component-state-information)
-   [Abrufen von Featurestatusinformationen](#obtaining-feature-state-information)

## <a name="enumerating-products"></a>Aufzählen von Produkten

Verwenden Sie die [**MsiEnumProductsEx-Funktion,**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) um Windows Installer-Anwendungen aufzuzählen, die im System installiert sind. Diese Funktion kann alle computer- und benutzerbezogenen Installationen von Anwendungen (verwaltet und nicht verwaltet) für den aktuellen Benutzer und andere Benutzer im System finden. Verwenden Sie den *dwContext-Parameter,* um den zu findenden Installationskontext anzugeben. Sie können einen oder eine beliebige Kombination der möglichen Installationskontexte angeben. Verwenden Sie den *szUserSid-Parameter,* um den Benutzerkontext der zu findenden Anwendungen anzugeben.

## <a name="enumerating-patches"></a>Aufzählen von Patches

Verwenden Sie die [**MsiEnumPatchesEx-Funktion,**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) um patches zu suchen, die für eine Anwendung angewendet wurden. Diese Funktion kann Patches finden, die für eine bestimmte Anwendung oder für alle Anwendungen im System angewendet wurden. Diese Funktion kann Patches finden, die auf alle Computerinstallationen und benutzerbezogenen Installationen von Anwendungen (verwaltet und nicht verwaltet) für den aktuellen Benutzer und andere Benutzer im System angewendet werden.

Sie können den Installationskontext und den Benutzerkontext verwenden, um die Patchenumeration auf einen bestimmten Kontext oder alle Kontexte zu beschränken. Verwenden Sie den *dwContext-Parameter,* um den zu findenden Installationskontext anzugeben. Sie können einen oder eine beliebige Kombination der möglichen Installationskontexte angeben. Verwenden Sie den *szUserSid-Parameter,* um den Benutzerkontext der zu findenden Anwendungen anzugeben.

**So aufzählen Sie Patches, die für alle Produkte angewendet werden, die von allen Benutzern im System angekündigt oder installiert wurden**

-   Rufen Sie die [**MsiEnumPatchesEx-Funktion**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) auf.
    -   Verwenden Sie **NULL** für den Wert des *szProductCode-Parameters.*
    -   Verwenden Sie "s-1-1-0" als Wert des *szUserSid-Parameters.*
    -   Verwenden Sie "MSIINSTALLCONTEXT \_ ALL" als Wert des *dwContext-Parameters.*

**So aufzählen Sie Patches, die für alle Produkte angewendet werden, die von allen Benutzern im System angekündigt oder installiert wurden**

1.  Rufen Sie die [**MsiEnumProductsEx-Funktion**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) auf.

    -   Verwenden Sie **NULL** für den Wert des *szProductCode-Parameters.*
    -   Verwenden Sie "s-1-1-0" als Wert des *szUserSid-Parameters.*
    -   Verwenden Sie "MSIINSTALLCONTEXT \_ ALL" als Wert des *dwContext-Parameters.*

    Die -Funktion stellt einen Produktcode, einen Benutzerkontext und einen Installationskontext für jede gefundene Anwendung bereit.

2.  Rufen Sie für jede anwendung, die in Schritt 1 aufzählt, [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) auf, um die Patches aufzuzählen.

    Verwenden Sie die Von [**MsiEnumProductsEx abgerufenen**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) Produktcodes, Benutzerkontexte und Installationskontexte für die Werte von *szProductCode,* *szUserSid* und *dwContext* sowie für jeden **MsiEnumProductsEx-Funktionsaufruf.**

## <a name="obtaining-product-information"></a>Abrufen von Produktinformationen

Verwenden Sie die [**MsiGetProductInfoEx-Funktion,**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) um Informationen zu Anwendungen abzurufen, die im System angekündigt oder installiert werden, und zu den Eigenschaften, die abgerufen werden können. Diese Funktion kann Informationen für eine Instanz einer Anwendung abrufen, die unter einem anderen Benutzerkonto als dem aktuellen Benutzer installiert ist, kann aber keine Instanz eines Produkts abfragen, das in einem nicht verwalteten Kontext pro Benutzer für ein anderes Benutzerkonto als den aktuellen Benutzer angekündigt wird.

Sie können den Installationskontext und den Benutzerkontext angeben, um Informationen für Anwendungen einzuschränken, die in einem bestimmten Kontext installiert sind. Verwenden Sie den *dwContext-Parameter,* um den zu findenden Installationskontext anzugeben. Sie können nur einen der möglichen Installationskontexte angeben. Verwenden Sie den *szUserSid-Parameter,* um den Benutzerkontext der zu findenden Anwendungen anzugeben.

## <a name="obtaining-patch-information"></a>Abrufen von Patchinformationen

Eine Anwendung kann die [**MsiGetPatchInfoEx-Funktion**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) aufrufen, um Informationen zur Anwendung eines Patches für eine angegebene Instanz eines Produkts abzufragen. Eigenschaften wie **LocalPackage,** [**Transformationen**](transforms.md)und **State** können mit dieser Funktion abgerufen werden. Nicht alle Eigenschaftswerte sind garantiert für benutzerspezifische, nicht verwaltete Anwendungen verfügbar, wenn der Benutzer derzeit nicht am Computer angemeldet ist. Sie können nur einen der möglichen Installationskontexte angeben.

Sie können den Installationskontext und den Benutzerkontext angeben, um Informationen auf Patches zu beschränken, die auf Anwendungen angewendet werden, die in einem bestimmten Kontext installiert sind. Verwenden Sie den *dwContext-Parameter,* um den zu findenden Installationskontext anzugeben. Sie können nur einen der möglichen Installationskontexte angeben. Verwenden Sie den *szUserSid-Parameter,* um den Benutzerkontext der zu findenden Anwendungen anzugeben.

## <a name="obtaining-component-state-information"></a>Abrufen von Komponentenzustandsinformationen

Anwendungen können die [**MsiQueryComponentState-Funktion**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea) aufrufen, um den installierten Zustand für eine Komponente abzurufen. Diese Funktion bestimmt, ob die Komponente lokal installiert oder installiert ist, um von der Quelle aus ausgeführt zu werden. Die Funktion kann eine Komponente einer Instanz einer Anwendung abfragen, die unter anderen Benutzerkonten als dem aktuellen Benutzer installiert ist, vorausgesetzt, dass das Produkt nicht im nicht verwalteten Kontext pro Benutzer für ein anderes Benutzerkonto als den aktuellen Benutzer angekündigt wird.

Sie können einen Installationskontext und einen Benutzerkontext angeben, um den Status von Komponenten für Anwendungen abzurufen, die in einem bestimmten Kontext installiert sind. Verwenden Sie den *dwContext-Parameter,* um den zu findenden Installationskontext anzugeben. Sie können nur einen der möglichen Installationskontexte angeben. Verwenden Sie den *szUserSid-Parameter,* um den Benutzerkontext der zu findenden Anwendungen anzugeben.

## <a name="obtaining-feature-state-information"></a>Abrufen von Featurestatusinformationen

Anwendungen können die [**MsiQueryFeatureStateEx-Funktion**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa) aufrufen, um den installierten Zustand für ein Produktfeature abzurufen. Diese Funktion bestimmt, ob das Feature angekündigt, lokal installiert oder installiert wird, um von der Quelle aus ausgeführt zu werden. Die -Funktion kann verwendet werden, um ein beliebiges Feature einer Instanz einer Anwendung abzufragen, die unter dem Computerkonto installiert ist, oder einen beliebigen Kontext unter dem aktuellen Benutzerkonto oder den pro Benutzer verwalteten Kontext unter einem anderen Benutzerkonto als dem aktuellen Benutzer. Diese Funktion kann keine Anwendung abfragen, die im nicht verwalteten Kontext pro Benutzer für ein anderes Benutzerkonto als den aktuellen Benutzer installiert ist. Sie können nur einen der möglichen Installationskontexte angeben.

Sie können einen Installationskontext und einen Benutzerkontext angeben, um den Status der Features für Anwendungen abzurufen, die in einem bestimmten Kontext installiert sind. Verwenden Sie den *dwContext-Parameter,* um den zu findenden Installationskontext anzugeben. Sie können nur einen der möglichen Installationskontexte angeben. Verwenden Sie den *szUserSid-Parameter,* um den Benutzerkontext der zu findenden Anwendungen anzugeben.

 

 



