---
description: Die Anpassungs Transformation kann in einem Speicher des Windows Installer Pakets gespeichert werden, um sicherzustellen, dass die Transformation immer verfügbar ist, wenn das Installationspaket verfügbar ist.
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: Einbetten von Anpassungs Transformationen als unter Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd275d36b37b2e29ae166a2a464a62495d2ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362527"
---
# <a name="embedding-customization-transforms-as-substorage"></a><span data-ttu-id="083bc-103">Einbetten von Anpassungs Transformationen als unter Speicher</span><span class="sxs-lookup"><span data-stu-id="083bc-103">Embedding Customization Transforms as Substorage</span></span>

<span data-ttu-id="083bc-104">Die Anpassungs Transformation kann in einem Speicher des Windows Installer Pakets gespeichert werden, um sicherzustellen, dass die Transformation immer verfügbar ist, wenn das Installationspaket verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="083bc-104">You may store the customization transform in a storage of the Windows Installer package to guarantee that the transform is always available when the installation package is available.</span></span> <span data-ttu-id="083bc-105">Siehe [eingebettete Transformationen](embedded-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="083bc-105">See [Embedded Transforms](embedded-transforms.md).</span></span> <span data-ttu-id="083bc-106">Ein Beispiel hierfür finden Sie im Windows Installer SDK als Dienstprogramm WiSubStg.vbs.</span><span class="sxs-lookup"><span data-stu-id="083bc-106">An example of this is provided in the Windows Installer SDK as the utility WiSubStg.vbs.</span></span> <span data-ttu-id="083bc-107">Der folgende Code Ausschnitt, Emb.vbs, veranschaulicht auch die Verwendung der [Tabelle Storages](-storages-table.md) zum Hinzufügen einer eingebetteten Transformation und ist für die Verwendung mit Windows Script Host vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="083bc-107">The following snippet, Emb.vbs, also illustrates the use of the [Storages table](-storages-table.md) to add an embedded transform and is for use with Windows Script Host.</span></span>


```VB
'Emb.vbs. Argument(0) is the original database. Argument(1) is the
'    path to the transform file. Argument(2) is the name of the storage.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
 WScript.Echo "Usage is emb.vbs [original database] [transform] [storage name]"
 WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
 
' Evaluate command-line arguments and set open and update modes
Dim databasePath: databasePath = Wscript.Arguments(0)
Dim importPath  : importPath = Wscript.Arguments(1)
Dim storageName : storageName = Wscript.Arguments(2)
 
' Open database and create a view on the _Storages table
Dim sqlQuery : sqlQuery = "SELECT `Name`,`Data` FROM _Storages"
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim view     : Set view = database.OpenView(sqlQuery)
 
'Create and Insert the row.
Dim record   : Set record = installer.CreateRecord(2)
record.StringData(1) = storageName
view.Execute record
 
'Insert storage - copy data into stream
record.SetStream 2, importPath
view.Modify 3, record
database.Commit
Set view = Nothing
Set database = Nothing
```



<span data-ttu-id="083bc-108">Wechseln Sie zum Hinzufügen eines Speichers mit dem Namen MNPtrans1 zu MNP2000.msi und mit der Transformation, die Sie unter [Hinzufügen von Zusammenfassungs Informationen zur Anpassungs Transformation](adding-summary-information-to-customization-transform.md)erstellt haben, um Verzeichnisse in den Ordner mit Emb.vbs, die ursprüngliche Datenbank und die Transformations Datei zu ändern, und geben Sie dann die folgende Befehlszeile ein</span><span class="sxs-lookup"><span data-stu-id="083bc-108">To add a storage named MNPtrans1 to MNP2000.msi, and containing the transform you created in [Adding Summary Information to Customization Transform](adding-summary-information-to-customization-transform.md), change directories to the folder containing Emb.vbs, the original database, and the transform file, then enter the following command line.</span></span>

<span data-ttu-id="083bc-109">**Cscript.exe Emb.vbs MNP2000.msi mnptrans. MST MNPtrans1**</span><span class="sxs-lookup"><span data-stu-id="083bc-109">**Cscript.exe Emb.vbs MNP2000.msi MNPtrans.mst MNPtrans1**</span></span>

<span data-ttu-id="083bc-110">Dadurch wird das Beispiel für die Anpassungs Transformation abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="083bc-110">This completes the customization transform example.</span></span> <span data-ttu-id="083bc-111">Nach dem Einbetten der Transformation in mnptrans. MST ist die Transformation immer mit dem Installationspaket verfügbar.</span><span class="sxs-lookup"><span data-stu-id="083bc-111">After embedding the transform in MNPtrans.mst, the transform is always available with the installation package.</span></span> <span data-ttu-id="083bc-112">Die Datei "mnptrans. mst" muss sich nicht an der Quelle befinden, um die Transformation anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="083bc-112">The file MNPtrans.mst does not need to be located at the source to apply the transform.</span></span>

<span data-ttu-id="083bc-113">Entfernen Sie mnptrans. MST aus dem Ordner, der das Beispiel Installationspaket enthält.</span><span class="sxs-lookup"><span data-stu-id="083bc-113">Remove MNPtrans.mst from the folder containing the sample installation package.</span></span> <span data-ttu-id="083bc-114">Klicken Sie auf das MNP2000.msi Symbol, um eine Installation zu starten, oder verwenden Sie die folgende Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="083bc-114">Click the MNP2000.msi icon to launch an install or use the following command line.</span></span>

<span data-ttu-id="083bc-115">**msiexec/i MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="083bc-115">**msiexec /i MNP2000.msi**</span></span>

<span data-ttu-id="083bc-116">Beachten Sie, dass dadurch das Produkt ohne Anpassungen installiert wird.</span><span class="sxs-lookup"><span data-stu-id="083bc-116">Note that this installs the product without the customizations.</span></span> <span data-ttu-id="083bc-117">Um mit den Anpassungen zu installieren, geben Sie die folgende Befehlszeile ein.</span><span class="sxs-lookup"><span data-stu-id="083bc-117">To install with the customizations, enter the following command line.</span></span> <span data-ttu-id="083bc-118">Verwenden Sie einen Doppelpunkt, um anzugeben, dass der Wert der [**Transformationen**](transforms.md) -Eigenschaft auf eine eingebettete Transformation verweist.</span><span class="sxs-lookup"><span data-stu-id="083bc-118">Use a colon to indicate that the value of the [**TRANSFORMS**](transforms.md) Property refers to an embedded transform.</span></span>

<span data-ttu-id="083bc-119">msiexec/i MNP2000.msi Transformationen =: MNPtrans1</span><span class="sxs-lookup"><span data-stu-id="083bc-119">msiexec /i MNP2000.msi TRANSFORMS=:MNPtrans1</span></span>

<span data-ttu-id="083bc-120">Beachten Sie, dass die Gate-Funktion nicht in der Funktionsauswahl Struktur angezeigt wird und dass die Komponenten der Gate-Funktion nicht installiert werden, auch wenn ein kompletter Installationstyp in der Benutzeroberfläche ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="083bc-120">Note that the Gate feature does not appear in the feature selection tree and that the components of the Gate feature are not installed even if a Complete type of installation is selected in the user interface.</span></span>

## <a name="next-example"></a><span data-ttu-id="083bc-121">Nächstes Beispiel</span><span class="sxs-lookup"><span data-stu-id="083bc-121">Next example</span></span>

[<span data-ttu-id="083bc-122">Beispiel für ein kleines Update-Patching</span><span class="sxs-lookup"><span data-stu-id="083bc-122">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)

 

 



