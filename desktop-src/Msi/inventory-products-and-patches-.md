---
description: 'Benutzer und Anwendungen mit Administratorrechten können Windows Installer-Funktionen verwenden, um die Windows Installer Anwendungen, Features, Komponenten und Patches, die auf dem System installiert sind, zu inventarisieren. Ab Windows Installer&\# 160; 3.0 können Benutzer und Anwendungen, die über Administratorrechte verfügen, die Windows Installer Anwendungen, Features, Komponenten und Patches auflisten, die von allen Benutzern auf dem System installiert werden. Administratoren und Anwendungen können Informationen zu einem Produkt oder Patch für einen bestimmten Benutzer oder für alle Benutzer im System abrufen. Anwendungen können den Funktionsstatus oder den Komponenten Zustand für einen bestimmten Benutzer abrufen. Die Inventur Funktionen, die ab Windows Installer&\# 160; 3.0 verfügbar sind, können den Umfang der gefundenen Elemente durch den Installations Kontext und den Benutzer Kontext einschränken. Es gibt drei mögliche Installations Kontexte: pro Benutzer, pro Computer und pro Benutzer verwaltet. Der Benutzer Kontext kann ein bestimmter Benutzer oder alle Benutzer des Systems sein. Die Versionen der Windows Installer Inventur Funktionen vor Windows Installer&\# 160; 3.0 können nur auf dem System installierte Elemente im Computer Kontext oder im kontextbezogenen Kontext des aktuellen Benutzers auflisten. Diese Einschränkung verhindert eine vollständige Inventur aller Windows Installer Produkte und Patches, die von anderen Benutzern als dem aktuellen Benutzer im System installiert werden. Auflisten von productsenumerating patchesbeschaffung Produktinformationen abrufen von Patchinformationen Abrufen von Informationen über den Status der Komponente'
ms.assetid: ef95c3c8-b4c8-4305-8aa2-07ec74b3121b
title: Verwenden von Windows Installer zum Inventarisieren von Produkten und Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7915a8a58954c2e07a3dae9536ed7bae399e416b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525163"
---
# <a name="using-windows-installer-to-inventory-products-and-patches"></a>Verwenden von Windows Installer zum Inventarisieren von Produkten und Patches

Benutzer und Anwendungen mit Administratorrechten können Windows Installer-Funktionen verwenden, um die Windows Installer Anwendungen, Features, Komponenten und Patches, die auf dem System installiert sind, zu inventarisieren.

Ab Windows Installer 3,0 können Benutzer und Anwendungen, die über Administratorrechte verfügen, die Windows Installer Anwendungen, Features, Komponenten und Patches auflisten, die von allen Benutzern auf dem System installiert werden. Administratoren und Anwendungen können Informationen zu einem Produkt oder Patch für einen bestimmten Benutzer oder für alle Benutzer im System abrufen. Anwendungen können den Funktionsstatus oder den Komponenten Zustand für einen bestimmten Benutzer abrufen.

Die Inventur Funktionen, die ab Windows Installer 3,0 verfügbar sind, können den Bereich der gefundenen Elemente durch den Installations Kontext und den Benutzer Kontext einschränken. Es gibt drei mögliche Installations Kontexte: pro Benutzer, pro Computer und pro Benutzer verwaltet. Der Benutzer Kontext kann ein bestimmter Benutzer oder alle Benutzer des Systems sein.

Die Versionen der Windows Installer Inventur Funktionen vor Windows Installer 3,0 können nur Elemente auflisten, die auf dem System im Computer Kontext oder im benutzerspezifischen Kontext des aktuellen Benutzers installiert sind. Diese Einschränkung verhindert eine vollständige Inventur aller Windows Installer Produkte und Patches, die von anderen Benutzern als dem aktuellen Benutzer im System installiert werden.

-   [Auflisten von Produkten](#enumerating-products)
-   [Auflisten von Patches](#enumerating-patches)
-   [Abrufen von Produktinformationen](#obtaining-product-information)
-   [Abrufen von Patchinformationen](#obtaining-patch-information)
-   [Abrufen von Komponenten Zustandsinformationen](#obtaining-component-state-information)
-   [Abrufen von Informationen zum Funktionsstatus](#obtaining-feature-state-information)

## <a name="enumerating-products"></a>Auflisten von Produkten

Verwenden Sie die Funktion " [**msienumproductsex**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) ", um Windows Installer Anwendungen aufzuzählen, die im System installiert sind. Diese Funktion kann alle Installationen pro Computer und benutzerspezifische Installationen von Anwendungen (verwaltet und nicht verwaltet) für den aktuellen Benutzer und andere Benutzer im System finden. Verwenden Sie den *dwcontext* -Parameter, um den zu gefundenen Installations Kontext anzugeben. Sie können eine beliebige Kombination der möglichen Installations Kontexte angeben. Verwenden Sie den *szusersid* -Parameter, um den Benutzer Kontext der gefundenen Anwendungen anzugeben.

## <a name="enumerating-patches"></a>Auflisten von Patches

Verwenden Sie die Funktion " [**msienenpatchesex**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) ", um auf eine Anwendung angewendete Patches zu suchen. Mit dieser Funktion können Patches gefunden werden, die für eine bestimmte Anwendung oder für alle Anwendungen im System angewendet wurden. Mit dieser Funktion können Sie Patches finden, die für den aktuellen Benutzer und andere Benutzer im System auf alle computerspezifischen Installationen und Anwendungen pro Benutzer angewendet werden (verwaltet und nicht verwaltet).

Sie können den Installations Kontext und den Benutzer Kontext verwenden, um die patchenumeration auf einen bestimmten Kontext oder auf alle Kontexte zu beschränken. Verwenden Sie den *dwcontext* -Parameter, um den zu gefundenen Installations Kontext anzugeben. Sie können eine beliebige Kombination der möglichen Installations Kontexte angeben. Verwenden Sie den *szusersid* -Parameter, um den Benutzer Kontext der gefundenen Anwendungen anzugeben.

**So zählen Sie Patches auf, die für alle von allen Benutzern im System angekündigten oder installierten Produkte angewendet wurden**

-   Aufrufen der Funktion " [**msienenpatchesex**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) ".
    -   Verwenden Sie für den Wert des *szproductcode* -Parameters **null** .
    -   Verwenden Sie "s-1-1-0" als Wert des Parameters " *szusersid* ".
    -   Verwenden Sie "msiinstallcontext \_ all" für den Wert des *dwcontext* -Parameters.

**So zählen Sie Patches auf, die für alle von allen Benutzern im System angekündigten oder installierten Produkte angewendet wurden**

1.  Ruft die [**msienenproductsex**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) -Funktion auf.

    -   Verwenden Sie für den Wert des *szproductcode* -Parameters **null** .
    -   Verwenden Sie "s-1-1-0" als Wert des Parameters " *szusersid* ".
    -   Verwenden Sie "msiinstallcontext \_ all" für den Wert des *dwcontext* -Parameters.

    Die-Funktion stellt einen Produktcode, einen Benutzer Kontext und einen Installations Kontext für jede gefundene Anwendung bereit.

2.  Für jede in Schritt 1 aufgeführte Anwendung müssen Sie [**msienumpatchesex**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) aufrufen, um die Patches aufzuzählen.

    Verwenden Sie die Produktcodes, Benutzer Kontexte und Installations Kontexte, die von [**msienüberproductsex**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) abgerufen wurden, um die Werte von *szproductcode*, *szusersid* und *dwcontext* sowie jeden **msienenproductsex** -Funktions aufzurufen.

## <a name="obtaining-product-information"></a>Abrufen von Produktinformationen

Verwenden Sie die Funktion [**msigetproductinfoex**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) zum Abrufen von Informationen zu Anwendungen, die im System angekündigt oder installiert werden, sowie zu den Eigenschaften, die abgerufen werden können. Diese Funktion kann Informationen für eine Instanz einer Anwendung erhalten, die unter einem anderen Benutzerkonto als dem aktuellen Benutzer installiert ist, aber eine Instanz eines Produkts, die unter einem nicht verwalteten Benutzerkonto für ein anderes Benutzerkonto als den aktuellen Benutzer angekündigt wird, kann nicht abgefragt werden.

Sie können den Installations Kontext und den Benutzer Kontext angeben, um Informationen zu den in einem bestimmten Kontext installierten Anwendungen einzuschränken. Verwenden Sie den *dwcontext* -Parameter, um den zu gefundenen Installations Kontext anzugeben. Sie können nur einen der möglichen Installations Kontexte angeben. Verwenden Sie den *szusersid* -Parameter, um den Benutzer Kontext der gefundenen Anwendungen anzugeben.

## <a name="obtaining-patch-information"></a>Abrufen von Patchinformationen

Eine Anwendung kann die [**msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) -Funktion aufrufen, um Informationen über die Anwendung eines Patches an eine angegebene Instanz eines Produkts abzufragen. Eigenschaften wie **localpackage**, [**Transformationen**](transforms.md)und **State** können mithilfe dieser Funktion abgerufen werden. Nicht alle Eigenschaftswerte sind garantiert für benutzerspezifische nicht verwaltete Anwendungen verfügbar, wenn der Benutzer derzeit nicht am Computer angemeldet ist. Sie können nur einen der möglichen Installations Kontexte angeben.

Sie können den Installations Kontext und den Benutzer Kontext angeben, um Informationen auf Patches zu beschränken, die auf Anwendungen angewendet werden, die in einem bestimmten Kontext installiert werden. Verwenden Sie den *dwcontext* -Parameter, um den zu gefundenen Installations Kontext anzugeben. Sie können nur einen der möglichen Installations Kontexte angeben. Verwenden Sie den *szusersid* -Parameter, um den Benutzer Kontext der gefundenen Anwendungen anzugeben.

## <a name="obtaining-component-state-information"></a>Abrufen von Komponenten Zustandsinformationen

Anwendungen können die [**msiquerycomponentstate**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea) -Funktion zum Abrufen des installierten Zustands für eine Komponente abrufen. Diese Funktion bestimmt, ob die Komponente lokal oder installiert ist, um von der Quelle ausgeführt zu werden. Die-Funktion kann eine Komponente einer Instanz einer Anwendung Abfragen, die unter Benutzerkonten mit Ausnahme des aktuellen Benutzers installiert ist, vorausgesetzt, dass das Produkt nicht im nicht verwalteten Kontext des Benutzers für ein anderes Benutzerkonto als den aktuellen Benutzer angekündigt wird.

Sie können einen Installations Kontext und einen Benutzer Kontext angeben, um den Status von Komponenten für Anwendungen zu erhalten, die in einem bestimmten Kontext installiert werden. Verwenden Sie den *dwcontext* -Parameter, um den zu gefundenen Installations Kontext anzugeben. Sie können nur einen der möglichen Installations Kontexte angeben. Verwenden Sie den *szusersid* -Parameter, um den Benutzer Kontext der gefundenen Anwendungen anzugeben.

## <a name="obtaining-feature-state-information"></a>Abrufen von Informationen zum Funktionsstatus

Anwendungen können die Funktion " [**msiqueryfeaturestateex**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa) " aufrufen, um den installierten Zustand für ein Produkt Feature zu erhalten. Diese Funktion bestimmt, ob die Funktion angekündigt, lokal installiert oder installiert wird, um von der Quelle ausgeführt zu werden. Die-Funktion kann verwendet werden, um beliebige Funktionen einer Instanz einer Anwendung, die unter dem Computer Konto installiert ist, oder einen beliebigen Kontext unter dem aktuellen Benutzerkonto oder den pro Benutzer verwalteten Kontext unter jedem anderen Benutzerkonto als dem aktuellen Benutzer abzufragen. Diese Funktion kann nicht nach einer Anwendung Abfragen, die unter dem nicht verwalteten Benutzer Kontext für ein anderes Benutzerkonto als den aktuellen Benutzer installiert ist. Sie können nur einen der möglichen Installations Kontexte angeben.

Sie können einen Installations Kontext und einen Benutzer Kontext angeben, um den Status von Features für Anwendungen zu erhalten, die in einem bestimmten Kontext installiert werden. Verwenden Sie den *dwcontext* -Parameter, um den zu gefundenen Installations Kontext anzugeben. Sie können nur einen der möglichen Installations Kontexte angeben. Verwenden Sie den *szusersid* -Parameter, um den Benutzer Kontext der gefundenen Anwendungen anzugeben.

 

 



