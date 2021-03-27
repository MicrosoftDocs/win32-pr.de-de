---
description: In diesem Thema wird erläutert, wie neue Dateitypen erstellt werden und wie Sie Ihre APP mit dem Dateityp und anderen klar definierten Dateitypen verknüpfen.
ms.assetid: 055648cd-46ce-4e61-80b2-bcf1d1823e20
title: Dateitypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d697c42626c6e1ab3e0b5cc0b88bd065523d53a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979744"
---
# <a name="file-types"></a><span data-ttu-id="a1580-103">Dateitypen</span><span class="sxs-lookup"><span data-stu-id="a1580-103">File Types</span></span>

<span data-ttu-id="a1580-104">In diesem Thema wird erläutert, wie neue Dateitypen erstellt werden und wie Sie Ihre APP mit dem Dateityp und anderen klar definierten Dateitypen verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="a1580-104">This topic explains how to create new file types and how to associate your app with your file type and other well-defined file types.</span></span> <span data-ttu-id="a1580-105">Dateien mit einer gemeinsamen Dateinamenerweiterung (doc, HTML usw.) weisen denselben *Typ* auf.</span><span class="sxs-lookup"><span data-stu-id="a1580-105">Files with a shared common file name extension (.doc, .html, and so on) are of the same *type*.</span></span> <span data-ttu-id="a1580-106">Wenn Sie z. b. einen neuen Text-Editor erstellen, können Sie den vorhandenen txt-Dateityp verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1580-106">For example, if you create a new text editor, then you can use the existing .txt file type.</span></span> <span data-ttu-id="a1580-107">In anderen Fällen müssen Sie möglicherweise einen neuen Dateityp erstellen.</span><span class="sxs-lookup"><span data-stu-id="a1580-107">In other cases, you might need to create a new file type.</span></span>

<span data-ttu-id="a1580-108">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="a1580-108">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="a1580-109">Öffentliche und private Dateitypen</span><span class="sxs-lookup"><span data-stu-id="a1580-109">Public and Private File Types</span></span>](#public-and-private-file-types)
-   [<span data-ttu-id="a1580-110">Registrieren eines Dateityps</span><span class="sxs-lookup"><span data-stu-id="a1580-110">Registering a File Type</span></span>](#registering-a-file-type)
    -   [<span data-ttu-id="a1580-111">Festlegen optionaler Unterschlüssel und Dateityp Erweiterungs Attribute</span><span class="sxs-lookup"><span data-stu-id="a1580-111">Setting Optional Subkeys and File Type Extension Attributes</span></span>](#setting-optional-subkeys-and-file-type-extension-attributes)
    -   [<span data-ttu-id="a1580-112">Löschen von Registrierungsinformationen während der deinstalstallation</span><span class="sxs-lookup"><span data-stu-id="a1580-112">Deleting Registry Information During Uninstallation</span></span>](#deleting-registry-information-during-uninstallation)
-   [<span data-ttu-id="a1580-113">Dateitypen, die offene Metadaten unterstützen</span><span class="sxs-lookup"><span data-stu-id="a1580-113">File Types That Support Open Metadata</span></span>](#file-types-that-support-open-metadata)
-   [<span data-ttu-id="a1580-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a1580-114">Related topics</span></span>](#related-topics)

<span data-ttu-id="a1580-115">Weitere Informationen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="a1580-115">Additional information can be found on the following topics:</span></span>

-   [<span data-ttu-id="a1580-116">Vorgehensweise beim Auswählen einer Dateityp Erweiterung</span><span class="sxs-lookup"><span data-stu-id="a1580-116">How To Choose a File Type Extension</span></span>](how-to-choose-a-file-type-extension.md)
-   [<span data-ttu-id="a1580-117">Definieren von Dateityp Attributen</span><span class="sxs-lookup"><span data-stu-id="a1580-117">How To Define File Type Attributes</span></span>](./how-to-define-file-type-attributes.md)
-   [<span data-ttu-id="a1580-118">Einschließen einer Anwendung im Dialog Feld "Öffnen mit"</span><span class="sxs-lookup"><span data-stu-id="a1580-118">How To Include an Application on the Open with Dialog Box</span></span>](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [<span data-ttu-id="a1580-119">Ausschließen einer Anwendung aus dem Dialog Feld "Öffnen mit" für nicht zugeordnete Dateitypen</span><span class="sxs-lookup"><span data-stu-id="a1580-119">How To Exclude an Application from the Open with Dialog Box for Unassociated File Types</span></span>](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)

## <a name="public-and-private-file-types"></a><span data-ttu-id="a1580-120">Öffentliche und private Dateitypen</span><span class="sxs-lookup"><span data-stu-id="a1580-120">Public and Private File Types</span></span>

<span data-ttu-id="a1580-121">Öffentliche Dateitypen werden auch als beliebte oder strittige Typen bezeichnet, da konkurrierende Anwendungen diesen Dateitypen zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="a1580-121">Public file types are also known as popular or contentious types because competing applications might want to be associated with these file types.</span></span> <span data-ttu-id="a1580-122">Zu den Merkmalen der öffentlichen Dateitypen gehören:</span><span class="sxs-lookup"><span data-stu-id="a1580-122">Characteristics of public file types include:</span></span>

-   <span data-ttu-id="a1580-123">Sie werden in der Regel in Standard Textteilen definiert und/oder werden von ihren definierenden Organisationen als Austauschformate herauf gestuft.</span><span class="sxs-lookup"><span data-stu-id="a1580-123">They are typically defined by standards bodies, and/or are promoted by their defining organizations as interchange formats.</span></span>
-   <span data-ttu-id="a1580-124">Sie werden häufig für verschiedene Zwecke zwischen Computern und Benutzern ausgetauscht.</span><span class="sxs-lookup"><span data-stu-id="a1580-124">They are often exchanged between computers and users for diverse purposes.</span></span>
-   <span data-ttu-id="a1580-125">Sie müssen auf vielen verschiedenen Plattformen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a1580-125">They need to be supported on many different platforms.</span></span>
-   <span data-ttu-id="a1580-126">Anwendungen von mehreren Anbietern werden diese wahrscheinlich verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a1580-126">Applications from multiple vendors are likely to handle them.</span></span>

<span data-ttu-id="a1580-127">Einige Beispiele für Dateitypen, die als öffentlich angesehen werden, sind die Bild Dateitypen PNG, GIF, JPG und BMP sowie die Audiotypen. wav,. MP3 und. au.</span><span class="sxs-lookup"><span data-stu-id="a1580-127">Some examples of file types that are considered public are the image file types .png, .gif, .jpg, and .bmp, and the audio types .wav, .mp3, and .au.</span></span>

<span data-ttu-id="a1580-128">Im Gegensatz zu öffentlichen Dateitypen verfügen private oder proprietäre Dateitypen in der Regel über ein Format, das nur von einer Anwendung oder einem Anbieter implementiert und verstanden wird.</span><span class="sxs-lookup"><span data-stu-id="a1580-128">Unlike public file types, private or proprietary file types typically have a format that is implemented and understood by only one application or vendor.</span></span> <span data-ttu-id="a1580-129">Folglich sind private Dateitypen in der Regel nicht anfällig für Konflikte zwischen Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="a1580-129">As a result, private file types are typically not prone to conflicts between applications.</span></span> <span data-ttu-id="a1580-130">Einige Dateitypen können als private Dateitypen gestartet werden, werden jedoch später zu öffentlichen Dateitypen.</span><span class="sxs-lookup"><span data-stu-id="a1580-130">Some file types can start as private file types but later become public file types.</span></span>

> [!Note]  
> <span data-ttu-id="a1580-131">Windows unterscheidet nicht zwischen öffentlichen und privaten Dateitypen.</span><span class="sxs-lookup"><span data-stu-id="a1580-131">Windows does not differentiate between public and private file types.</span></span> <span data-ttu-id="a1580-132">Der Unterschied ist nur wichtig, um Entscheidungen über die Wahl der Dateityp Registrierung zu treffen.</span><span class="sxs-lookup"><span data-stu-id="a1580-132">The distinction is relevant only in making decisions about your choice of file type registration.</span></span>

 

## <a name="registering-a-file-type"></a><span data-ttu-id="a1580-133">Registrieren eines Dateityps</span><span class="sxs-lookup"><span data-stu-id="a1580-133">Registering a File Type</span></span>

<span data-ttu-id="a1580-134">Um den Dateityp einer vorhandenen Anwendung zuzuordnen, suchen Sie die Anwendungs ProgID in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="a1580-134">To associate the file type with an existing application, locate the application ProgID in the registry.</span></span> <span data-ttu-id="a1580-135">Um den Dateityp einer neuen Anwendung zuzuordnen, definieren Sie eine ProgID für Ihre Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a1580-135">To associate the file type with a new application, define a ProgID for your application.</span></span> <span data-ttu-id="a1580-136">Weitere Informationen zum Definieren einer neuen ProgID [finden Sie](fa-progids.md)Unterprogramm gesteuerte Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a1580-136">For information about defining a new ProgID, see [Programmatic Identifiers](fa-progids.md).</span></span>

<span data-ttu-id="a1580-137">Die Unterschlüssel der Dateinamenerweiterung weisen die folgende allgemeine Form auf: *Erweiterung* = *ProgID*.</span><span class="sxs-lookup"><span data-stu-id="a1580-137">File name extension subkeys have the following general form: *extension*=*ProgID*.</span></span> <span data-ttu-id="a1580-138">Die Unterschlüssel der Dateinamenerweiterung werden in der Stamm Struktur der **HKEY- \_ Klassen \_** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a1580-138">File name extension subkeys are stored in the **HKEY\_CLASSES\_ROOT** subtree.</span></span>

<span data-ttu-id="a1580-139">Beim Erstellen von Dateityp unter Schlüsseln in der Registrierung ist es wichtig, den führenden Zeitraum (.) einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="a1580-139">It is important to include the leading period (.) when creating file type subkeys in the registry.</span></span> <span data-ttu-id="a1580-140">Wenn Sie z. b. möchten, dass ein Dateityp mit der kurzen Erweiterung. MYP und der Long-Erweiterung. MYP-File mit einer Anwendung namens myprogram geöffnet wird, verwenden Sie die folgende Syntax:</span><span class="sxs-lookup"><span data-stu-id="a1580-140">For example, if you want a file type with the short extension .myp and the long extension .myp-file to be opened with an application called MyProgram, use the following syntax:</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = ApplicationVendor.MyProgram
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
```

<span data-ttu-id="a1580-141">Wie im vorherigen Beispiel gezeigt, sollten Sie, wenn Sie auch eine kurze Dateinamenerweiterung (. MYP) registrieren, einen Unterschlüssel für die Long-Erweiterung (MYP-Datei) erstellen.</span><span class="sxs-lookup"><span data-stu-id="a1580-141">As demonstrated in the preceding example, if you also register a short file name extension (.myp), you should create a subkey for the long extension (.myp-file) as well.</span></span> <span data-ttu-id="a1580-142">Weitere Informationen finden Sie unter [Dateityp Handler](fa-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a1580-142">For more information, see [File Type Handlers](fa-file-extensions.md).</span></span>

### <a name="setting-optional-subkeys-and-file-type-extension-attributes"></a><span data-ttu-id="a1580-143">Festlegen optionaler Unterschlüssel und Dateityp Erweiterungs Attribute</span><span class="sxs-lookup"><span data-stu-id="a1580-143">Setting Optional Subkeys and File Type Extension Attributes</span></span>

<span data-ttu-id="a1580-144">Dateityp-Erweiterungs Einträge in der Registrierung verfügen über mehrere optionale Unterschlüssel und Attribute.</span><span class="sxs-lookup"><span data-stu-id="a1580-144">File type extension entries in the registry have several optional subkeys and attributes.</span></span>

<span data-ttu-id="a1580-145">Die von Dateizuordnungen verwendeten Dateityp-Erweiterungs Einträge werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a1580-145">The file type extension entries that are used by file associations are described in the following table.</span></span> <span data-ttu-id="a1580-146">Alle Werte sind vom Typ " **reg \_ SZ** ".</span><span class="sxs-lookup"><span data-stu-id="a1580-146">All values are of the **REG\_SZ** type.</span></span>



| <span data-ttu-id="a1580-147">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="a1580-147">Registry entry</span></span>  | <span data-ttu-id="a1580-148">Action</span><span class="sxs-lookup"><span data-stu-id="a1580-148">Action</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1580-149">Standard</span><span class="sxs-lookup"><span data-stu-id="a1580-149">Default</span></span>         | <span data-ttu-id="a1580-150">Legen Sie den Standardwert des Erweiterungs unter Schlüssels auf die ProgID fest, mit der er verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a1580-150">Set the default value of the extension subkey to the ProgID to which it is linked.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a1580-151">Inhaltstyp</span><span class="sxs-lookup"><span data-stu-id="a1580-151">Content Type</span></span>    | <span data-ttu-id="a1580-152">Legen Sie den Wert Inhaltstyp auf den MIME-Inhaltstyp des Dateityps fest.</span><span class="sxs-lookup"><span data-stu-id="a1580-152">Set the Content Type value to the file type's MIME content type.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="a1580-153">OpenWithList</span><span class="sxs-lookup"><span data-stu-id="a1580-153">OpenWithList</span></span>    | <span data-ttu-id="a1580-154">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1580-154">Do not use.</span></span> <span data-ttu-id="a1580-155">Dieser Unterschlüssel enthält mindestens einen Anwendungs Unterschlüssel für Anwendungen, die im Dialogfeld **Öffnen mit** für den Dateityp angezeigt werden, und ist nur für exe-Anwendungen auf Betriebssystemen vor Windows XP vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="a1580-155">This subkey contains one or more application subkeys for applications that appear in the **Open with** dialog box entry for the file type and is intended only for .exe applications on operating systems prior to Windows XP.</span></span> <span data-ttu-id="a1580-156">Verwenden Sie stattdessen OpenWithProgIds.</span><span class="sxs-lookup"><span data-stu-id="a1580-156">Use OpenWithProgIds instead.</span></span>                                                            |
| <span data-ttu-id="a1580-157">OpenWithProgIds</span><span class="sxs-lookup"><span data-stu-id="a1580-157">OpenWithProgIds</span></span> | <span data-ttu-id="a1580-158">Dieser Unterschlüssel enthält eine Liste alternativer ProgIDs für diesen Dateityp.</span><span class="sxs-lookup"><span data-stu-id="a1580-158">This subkey contains a list of alternate ProgIDs for this file type.</span></span> <span data-ttu-id="a1580-159">Die Programme für diese ProgIDs werden im Menü **Öffnen mit** angezeigt und sind als Standard-Windows Store-Apps für den Dateityp verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a1580-159">The programs for these ProgIDs appear in the **Open with** menu and are available as default Windows Store apps for the file type.</span></span> <span data-ttu-id="a1580-160">Wenn eine Anwendung diesen Dateityp durch Ändern des Standardwerts übernimmt, sollte dieser Liste auch ein Eintrag hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a1580-160">Whenever an application takes over this file type by changing the default value, it should also add an entry to this list.</span></span> |
| <span data-ttu-id="a1580-161">Wahrnehmungstyp</span><span class="sxs-lookup"><span data-stu-id="a1580-161">PerceivedType</span></span>   | <span data-ttu-id="a1580-162">Legen Sie den Wert von "wahrnehmvedtype" auf den "wahrnehmvedtype" fest, zu dem die Datei gehört, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a1580-162">Set the PerceivedType value to the PerceivedType to which the file belongs, if any.</span></span> <span data-ttu-id="a1580-163">Diese Zeichenfolge wird von Windows-Versionen vor Windows Vista nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a1580-163">This string is not used by Windows versions prior to Windows Vista.</span></span> <span data-ttu-id="a1580-164">Weitere Informationen finden Sie unter [wahrgenommene Typen und Anwendungs Registrierung](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="a1580-164">For more information, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>                                                                           |



 

<span data-ttu-id="a1580-165">Die allgemeine Form des unter Schlüssels für die Dateinamenerweiterung lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="a1580-165">The general form of a file name extension subkey is as follows.</span></span> <span data-ttu-id="a1580-166">Alle Eintrags Typen haben den Typ " **reg \_ SZ** ".</span><span class="sxs-lookup"><span data-stu-id="a1580-166">All entry types are of the **REG\_SZ** type.</span></span>

```
HKEY_CLASSES_ROOT
   .ext
      (Default) = ProgID.ext.1
      Content Type = MIME content type
      PerceivedType = PerceivedType
      OpenWithProgids
         ProgID2.ext.1
         ProgID3.ext.1
      ProgID.ext.1
         shellnew
```

<span data-ttu-id="a1580-167">Wichtige Überlegungen zu Dateitypen:</span><span class="sxs-lookup"><span data-stu-id="a1580-167">Important considerations about file types include:</span></span>

-   <span data-ttu-id="a1580-168">Die Stamm Unterstruktur der **HKEY- \_ Klassen \_** ist eine Ansicht, die durch Zusammenführen von **aktuellen HKEY- \_ \_ Benutzer** \\ **Software** \\ **Klassen** und **HKEY- \_ \_** \\ **Software** \\ **Klassen** für lokale Computer</span><span class="sxs-lookup"><span data-stu-id="a1580-168">The **HKEY\_CLASSES\_ROOT** subtree is a view formed by merging **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** and **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Classes**</span></span>
-   <span data-ttu-id="a1580-169">Im Allgemeinen ist der Stamm der **HKEY- \_ Klassen \_** das Lesen aus, aber nicht das Schreiben in.</span><span class="sxs-lookup"><span data-stu-id="a1580-169">In general, **HKEY\_CLASSES\_ROOT** is intended to be read from but not written to.</span></span> <span data-ttu-id="a1580-170">Weitere Informationen finden Sie im Stamm Artikel [HKEY \_ Classes \_ ](../sysinfo/hkey-classes-root-key.md) .</span><span class="sxs-lookup"><span data-stu-id="a1580-170">For more information, see the [HKEY\_CLASSES\_ROOT](../sysinfo/hkey-classes-root-key.md) article.</span></span>
-   <span data-ttu-id="a1580-171">Um einen Dateityp Global auf einem bestimmten Computer zu registrieren, erstellen Sie einen Eintrag für den Dateityp im Unterschlüssel **HKEY \_ local \_ Machine** \\  \\ **Classes Software Classes** .</span><span class="sxs-lookup"><span data-stu-id="a1580-171">To register a file type globally on a particular computer, create an entry for the file type in the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Classes** subkey.</span></span>
-   <span data-ttu-id="a1580-172">Wenn Sie eine Dateityp Registrierung nur für den aktuellen Benutzer sichtbar machen möchten, erstellen Sie im Unterschlüssel **HKEY \_ Current \_ User** \\ **Software** \\ **Classes** einen Eintrag für den Dateityp.</span><span class="sxs-lookup"><span data-stu-id="a1580-172">To make a file type registration visible to the current user only, create an entry for the file type in the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span>
-   <span data-ttu-id="a1580-173">Eine Anwendung kann eine eigene Implementierung eines Verbs bereitstellen, wie z. b. "Open" oder "Play", wie im folgenden Registrierungs Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a1580-173">An application can provide its own implementation of a verb, such as open or play, as shown in the following registry example.</span></span>

    ```
    HKEY_CLASSES_ROOT
       Applications
          ApplicationName.exe
             shell
                verb
    ```

    <span data-ttu-id="a1580-174">Zu den unter Schlüsseln des Verb-unter Schlüssels gehören die Befehlszeile und die Drop Target-Methode: **Command** und **DropTarget**.</span><span class="sxs-lookup"><span data-stu-id="a1580-174">Subkeys of the verb subkey include the command line and the drop target method: **command** and **DropTarget**.</span></span>

-   <span data-ttu-id="a1580-175">Wenn Sie eine Datei Zuordnung erstellen oder ändern, ist es wichtig, das System zu benachrichtigen, dass Sie eine Änderung vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="a1580-175">When you create or change a file association, it is important to notify the system that you have made a change.</span></span> <span data-ttu-id="a1580-176">Rufen Sie hierzu " [**shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) " auf, und geben Sie das **shcne-Ereignis " \_ assocchanged** " an.</span><span class="sxs-lookup"><span data-stu-id="a1580-176">Do so by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) and specifying the **SHCNE\_ASSOCCHANGED** event.</span></span> <span data-ttu-id="a1580-177">Wenn Sie **shchangenotify** nicht aufrufen, wird die Änderung möglicherweise erst erkannt, nachdem das System neu gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="a1580-177">If you do not call **SHChangeNotify**, the change may not be recognized until after the system is rebooted.</span></span>
-   <span data-ttu-id="a1580-178">Zum Abrufen von Registrierungsinformationen bezüglich einer Datei Zuordnung verwenden Sie die [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a1580-178">To retrieve registry information regarding a file association, use the [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface.</span></span> <span data-ttu-id="a1580-179">Ein Szenario, in dem diese Vorgehensweise veranschaulicht wird, finden Sie unter [Beispielszenario für Datei](fa-sample-scenarios.md)Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="a1580-179">For a scenario that illustrates this procedure, see [File Association Sample Scenario](fa-sample-scenarios.md).</span></span>

> [!Note]  
> <span data-ttu-id="a1580-180">Die Registrierungs Unterschlüssel **App-Pfade** und **Anwendungen** werden verwendet, um das Verhalten des Systems im Auftrag von Anwendungen zu registrieren und zu steuern.</span><span class="sxs-lookup"><span data-stu-id="a1580-180">Both the **App Paths** and **Applications** registry subkeys are used to register and control the behavior of the system on behalf of applications.</span></span> <span data-ttu-id="a1580-181">Ausführlichere Informationen zu dieser Funktion finden Sie unter [Anwendungs Registrierung](app-registration.md).</span><span class="sxs-lookup"><span data-stu-id="a1580-181">For more detailed information about this functionality, see [Application Registration](app-registration.md).</span></span>

 

### <a name="deleting-registry-information-during-uninstallation"></a><span data-ttu-id="a1580-182">Löschen von Registrierungsinformationen während der deinstalstallation</span><span class="sxs-lookup"><span data-stu-id="a1580-182">Deleting Registry Information During Uninstallation</span></span>

<span data-ttu-id="a1580-183">Beim Deinstallieren einer Anwendung sollten die ProgIDs und die meisten anderen Registrierungsinformationen, die dieser Anwendung zugeordnet sind, im Rahmen der deinstallieren gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="a1580-183">When uninstalling an application, the ProgIDs and most other registry information associated with that application should be deleted as part of the uninstallation.</span></span> <span data-ttu-id="a1580-184">Anwendungen, die den Besitz eines Dateityps übernommen haben (indem Sie den Standardwert der **HKEY- \_ Klassen " \_ root**. Extension" des Dateityps \\  für die ProgID der Anwendung festlegen), sollten diesen Wert beim Deinstallieren nicht entfernen.</span><span class="sxs-lookup"><span data-stu-id="a1580-184">However, applications that have taken ownership of a file type (by setting the Default value of the file type's **HKEY\_CLASSES\_ROOT**\\ *.extension* subkey to the ProgID of the application) should not attempt to remove that value when uninstalling.</span></span> <span data-ttu-id="a1580-185">Wenn die Daten für den Standardwert nicht vorhanden sind, wird vermieden, dass Sie feststellen, ob eine andere Anwendung den Besitz des Dateityps übernommen hat, und den Standardwert überschrieben haben, nachdem die ursprüngliche Anwendung installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a1580-185">Leaving the data in place for the Default value avoids the difficulty of determining whether another application has taken ownership of the file type and overwritten the Default value after the original application was installed.</span></span> <span data-ttu-id="a1580-186">Windows respektiert den Standardwert nur dann, wenn die ProgID gefunden wurde, die eine registrierte ProgID enthält.</span><span class="sxs-lookup"><span data-stu-id="a1580-186">Windows respects the Default value only if the ProgID found there is a registered ProgID.</span></span> <span data-ttu-id="a1580-187">Wenn die Registrierung der ProgID aufgehoben wird, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a1580-187">If the ProgID is unregistered, it is ignored.</span></span>

<span data-ttu-id="a1580-188">Beachten Sie, dass weitere Besitz Informationen für den Dateityp in der **aktuellen HKEY- \_ \_ Benutzer** Unterstruktur gespeichert werden und nur dann verwendet werden, wenn die Anwendung, auf die verwiesen wird, registriert ist.</span><span class="sxs-lookup"><span data-stu-id="a1580-188">Note that other file-type ownership information is stored in the **HKEY\_CURRENT\_USER** subtree and also is used only when the application that it references is registered.</span></span> <span data-ttu-id="a1580-189">Daher müssen diese Daten beim Deinstallieren einer Anwendung nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a1580-189">Therefore, this data does not need to be removed when uninstalling an application.</span></span>

<span data-ttu-id="a1580-190">Im folgenden Beispiel wird der Status der Registrierung angezeigt, bevor eine Anwendung deinstalliert wird:</span><span class="sxs-lookup"><span data-stu-id="a1580-190">As an example, the following shows the state of the registry before an application is uninstalled:</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID
      shell
         open
            command
               (Default) = yourapp.exe %1
```

<span data-ttu-id="a1580-191">Im folgenden wird der Zustand der gleichen Registrierungseinträge nach der Installation der Anwendung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a1580-191">The following shows the state of those same registry entries after the application has been uninstalled.</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID subkey removed
```

## <a name="file-types-that-support-open-metadata"></a><span data-ttu-id="a1580-192">Dateitypen, die offene Metadaten unterstützen</span><span class="sxs-lookup"><span data-stu-id="a1580-192">File Types That Support Open Metadata</span></span>

<span data-ttu-id="a1580-193">In Windows 7 und höher unterstützen die folgenden Dateitypen geöffnete Metadaten.</span><span class="sxs-lookup"><span data-stu-id="a1580-193">In Windows 7 and later, the following file types support open metadata.</span></span>



| <span data-ttu-id="a1580-194">Dateityp</span><span class="sxs-lookup"><span data-stu-id="a1580-194">File type</span></span>                                                               | <span data-ttu-id="a1580-195">Dateinamen Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="a1580-195">File name extensions</span></span>                                          |
|-------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a1580-196">Office 2007-Dokumente</span><span class="sxs-lookup"><span data-stu-id="a1580-196">Office 2007 Documents</span></span>                                                   | <span data-ttu-id="a1580-197">. docx,. xlsx,. pptx</span><span class="sxs-lookup"><span data-stu-id="a1580-197">.docx, .xlsx, .pptx</span></span>                                           |
| <span data-ttu-id="a1580-198">Office 97-2003-Dokumente</span><span class="sxs-lookup"><span data-stu-id="a1580-198">Office 97-2003 Documents</span></span>                                                | <span data-ttu-id="a1580-199">. doc,. xls,. ppt</span><span class="sxs-lookup"><span data-stu-id="a1580-199">.doc, .xls, .ppt</span></span>                                              |
| <span data-ttu-id="a1580-200">Gespeicherte Suche</span><span class="sxs-lookup"><span data-stu-id="a1580-200">Saved Search</span></span>                                                            | <span data-ttu-id="a1580-201">. Search-MS</span><span class="sxs-lookup"><span data-stu-id="a1580-201">.search-ms</span></span>                                                    |
| <span data-ttu-id="a1580-202">Windows Media-basierte Formate (Advanced Streaming Format (ASF)-Container)</span><span class="sxs-lookup"><span data-stu-id="a1580-202">Windows Media-based formats (Advanced Streaming Format (ASF) container)</span></span> | <span data-ttu-id="a1580-203">WMV,. WMA</span><span class="sxs-lookup"><span data-stu-id="a1580-203">.wmv, .wma</span></span>                                                    |
| <span data-ttu-id="a1580-204">MP4 (Eigenschaften Handler)</span><span class="sxs-lookup"><span data-stu-id="a1580-204">MP4 (property handler)</span></span>                                                  | <span data-ttu-id="a1580-205">. MP4,. m4a,. m4v,. MP4V,. m4p,. M4B,. 3GP,. 3GPP,. 3gp2,. mov</span><span class="sxs-lookup"><span data-stu-id="a1580-205">.mp4, .m4a, .m4v, .mp4v, .m4p, .m4b, .3gp, .3gpp, .3gp2, .mov</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a1580-206">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a1580-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1580-207">Anwendungs Registrierung</span><span class="sxs-lookup"><span data-stu-id="a1580-207">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="a1580-208">Funktionsweise von Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="a1580-208">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="a1580-209">Inhaltsansicht nach Dateityp oder-Art</span><span class="sxs-lookup"><span data-stu-id="a1580-209">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="a1580-210">Dateityp Überprüfung</span><span class="sxs-lookup"><span data-stu-id="a1580-210">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="a1580-211">Dateityp Handler</span><span class="sxs-lookup"><span data-stu-id="a1580-211">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="a1580-212">Programmgesteuerte Bezeichner</span><span class="sxs-lookup"><span data-stu-id="a1580-212">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="a1580-213">Wahrgenommene Typen</span><span class="sxs-lookup"><span data-stu-id="a1580-213">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="a1580-214">Zuordnungs Arrays</span><span class="sxs-lookup"><span data-stu-id="a1580-214">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
