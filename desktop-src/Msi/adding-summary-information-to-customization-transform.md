---
description: Wenn Sie die Anpassungs Transformation während einer Installation des Produkts anwenden möchten, müssen Sie der Transformations Datei mnptrans. MST, die beim Generieren einer Anpassungs Transformation generiert wurde, einen Zusammenfassungs Informationsdaten Strom hinzufügen.
ms.assetid: 586f6c43-7449-4d06-9201-9b4b4919871e
title: Hinzufügen von Zusammenfassungs Informationen zur Anpassungs Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64957fcf8f29ab8793517015c7018292ba9a6e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348556"
---
# <a name="adding-summary-information-to-customization-transform"></a><span data-ttu-id="e7410-103">Hinzufügen von Zusammenfassungs Informationen zur Anpassungs Transformation</span><span class="sxs-lookup"><span data-stu-id="e7410-103">Adding Summary Information to Customization Transform</span></span>

<span data-ttu-id="e7410-104">Wenn Sie die Anpassungs Transformation während einer Installation des Produkts anwenden möchten, müssen Sie der Transformations Datei mnptrans. MST, die beim [Generieren einer Anpassungs Transformation](generating-a-customization-transform.md)generiert wurde, einen [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e7410-104">To apply the customization transform during an installation of the product, you must add a [Summary Information Stream](summary-information-stream.md) to the transform file MNPtrans.mst generated in [Generating a Customization Transform](generating-a-customization-transform.md).</span></span>

<span data-ttu-id="e7410-105">Sie können zusammenfassende Informationen für eine Transformation mithilfe von " [**msikreatetransformsummaryinfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) " oder der [**Methode "kreatetransformsummaryinfo**](database-createtransformsummaryinfo.md)" generieren.</span><span class="sxs-lookup"><span data-stu-id="e7410-105">You may generate summary information for a transform using [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) or the [**CreateTransformSummaryInfo Method**](database-createtransformsummaryinfo.md).</span></span> <span data-ttu-id="e7410-106">Der folgende Code Ausschnitt, Sum.vbs, veranschaulicht die [**Methode**](database-createtransformsummaryinfo.md) "" der Methode "Methode" und "Windows Script Host".</span><span class="sxs-lookup"><span data-stu-id="e7410-106">The following snippet, Sum.vbs, illustrates the [**CreateTransformSummaryInfo Method**](database-createtransformsummaryinfo.md) and is for use with Windows Script Host.</span></span> <span data-ttu-id="e7410-107">Beachten Sie, dass in diesem Beispiel keine Validierung durchführt und keine Fehlerbedingungen unterdrückt werden.</span><span class="sxs-lookup"><span data-stu-id="e7410-107">Note that this example performs no validation and suppresses no error conditions.</span></span>


```VB
'Sum.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is sum.vbs [original database] [customized database] [transform]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
 
' Open databases and transform 
Dim database1 : Set database1 =
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 =
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
Dim transform : transform = Wscript.Arguments(2)
 
' Create and add Summary Information
Dim transinfo : transinfo =
    Database2.CreateTransformSummaryInfo(Database1, transform,0,0)
```



<span data-ttu-id="e7410-108">Zum Erstellen und Hinzufügen von Zusammenfassungs Informationen zur Transformations Datei mnptrans. MST, die Sie beim Erstellen [einer Anpassungs Transformation](generating-a-customization-transform.md)erstellt haben, ändern Sie die Verzeichnisse in den Ordner, der Gen.vbs enthält, die ursprüngliche Datenbank, die aktualisierte Datenbank und die Transformation, und geben Sie die folgende Befehlszeile ein.</span><span class="sxs-lookup"><span data-stu-id="e7410-108">To create and add summary information to the transform file MNPtrans.mst you created in [Generating a Customization Transform](generating-a-customization-transform.md), change directories to the folder containing Gen.vbs, the original database, the updated database, and the transform, and enter the following command line.</span></span>

<span data-ttu-id="e7410-109">**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi mnptrans. MST**</span><span class="sxs-lookup"><span data-stu-id="e7410-109">**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans.mst**</span></span>

<span data-ttu-id="e7410-110">Klicken Sie auf das MNP2000.msi Symbol, um eine Installation zu starten, oder verwenden Sie die folgende Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="e7410-110">Click the MNP2000.msi icon to launch an install or use the following command line.</span></span>

<span data-ttu-id="e7410-111">**msiexec/i MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="e7410-111">**msiexec /i MNP2000.msi**</span></span>

<span data-ttu-id="e7410-112">Dadurch wird das Produkt ohne Anpassungen installiert.</span><span class="sxs-lookup"><span data-stu-id="e7410-112">This installs the product without the customizations.</span></span> <span data-ttu-id="e7410-113">Um mit der Anpassung zu installieren, geben Sie die folgende Befehlszeile ein.</span><span class="sxs-lookup"><span data-stu-id="e7410-113">To install with the customization, enter the following command line.</span></span> <span data-ttu-id="e7410-114">Beachten Sie, dass sich der Wert der [**Transformationen**](transforms.md) -Eigenschaft auf die Transformations Datei bezieht, die sich in der Quelle befindet.</span><span class="sxs-lookup"><span data-stu-id="e7410-114">Note that the value of the [**TRANSFORMS**](transforms.md) Property refers to transform file located at the source.</span></span>

<span data-ttu-id="e7410-115">**msiexec/i MNP2000.msi Transformationen = mnptrans. MST**</span><span class="sxs-lookup"><span data-stu-id="e7410-115">**msiexec /i MNP2000.msi TRANSFORMS=MNPtrans.mst**</span></span>

<span data-ttu-id="e7410-116">Das Gate-Feature wird nicht in der Funktionsauswahl Struktur angezeigt, und die Komponenten der Gate-Funktion werden nicht installiert, auch wenn auf der Benutzeroberfläche ein kompletter Installationstyp ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="e7410-116">The Gate feature does not appear in the feature selection tree and the components of the Gate feature are not installed even if a Complete type of installation is selected in the user interface.</span></span>

[<span data-ttu-id="e7410-117">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="e7410-117">Continue</span></span>](embedding-customization-transforms-as-substorage.md)

 

 



