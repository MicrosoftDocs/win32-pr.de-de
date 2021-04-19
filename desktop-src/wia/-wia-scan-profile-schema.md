---
description: Das Überprüfungs Profil Schema definiert ein XML-Format, das verwendet werden kann, um die Eigenschaften von Elementen der Windows-Abbild Erfassung (WIA), wie z. b. Scanner und Kameras, zu speichern.
ms.assetid: e0848db3-652a-45be-a18b-99b82420c586
title: Profil Schema überprüfen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331c52e933e1e6b771c477bdc8a38f1c5f749448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349011"
---
# <a name="scan-profile-schema"></a><span data-ttu-id="74dab-103">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="74dab-103">Scan Profile Schema</span></span>

<span data-ttu-id="74dab-104">Das Überprüfungs Profil Schema definiert ein XML-Format, das verwendet werden kann, um die Eigenschaften von Elementen der Windows-Abbild Erfassung (WIA), wie z. b. Scanner und Kameras, zu speichern.</span><span class="sxs-lookup"><span data-stu-id="74dab-104">The Scan Profile Schema defines an XML format that can be used to store the properties of Windows Image Acquisition (WIA) items, such as scanners and cameras.</span></span> <span data-ttu-id="74dab-105">Mit diesen permanenten Dateien können Anwendungen automatische Scans bereitstellen, ohne dass sich die Benutzer an die Eigenschafts Einstellungen der Elemente erinnern müssen.</span><span class="sxs-lookup"><span data-stu-id="74dab-105">These persistent files enable applications to provide automatic scanning without requiring users to remember the property settings of the items.</span></span>

<span data-ttu-id="74dab-106">Jedes [**IWiaItem2**](-wia-iwiaitem2.md) -Gerät kann über ein Überprüfungs Profil verfügen.</span><span class="sxs-lookup"><span data-stu-id="74dab-106">Any [**IWiaItem2**](-wia-iwiaitem2.md) device can have a scan profile.</span></span> <span data-ttu-id="74dab-107">Allerdings können **IWiaItem2** Items von Typen, \_ die mit einer Kategorie \_ fertiggestellt \_ wurden, die Datei fertiggestellt \_ \_ haben</span><span class="sxs-lookup"><span data-stu-id="74dab-107">However, **IWiaItem2** items of types WIA\_CATEGORY\_FINISHED\_FILE and WIA\_CATEGORY\_ROOT cannot have profiles.</span></span>

<span data-ttu-id="74dab-108">Scan Profile werden über die Schnittstellen [**iscanprofile**](-wia-iscanprofile.md), [**iscanprofilemgr**](-wia-iscanprofilemgr.md)und [**iscanprofileui**](-wia-iscanprofileui.md) erstellt und verwaltet.</span><span class="sxs-lookup"><span data-stu-id="74dab-108">Scan profiles are created and managed through the [**IScanProfile**](-wia-iscanprofile.md), [**IScanProfileMgr**](-wia-iscanprofilemgr.md), and [**IScanProfileUI**](-wia-iscanprofileui.md) interfaces.</span></span> <span data-ttu-id="74dab-109">Benutzer Ihrer Anwendung können Profile in eingeschränkter Weise mithilfe der [**iscanprofileui:: scanprofiledialog**](-wia-iscanprofileui-scanprofiledialog.md) -Methode ändern.</span><span class="sxs-lookup"><span data-stu-id="74dab-109">Users of your application can modify profiles in limited ways using the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="74dab-110">Alle Scan Profile verfügen über die folgenden Elemente: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , und `<Properties>` .</span><span class="sxs-lookup"><span data-stu-id="74dab-110">All scan profiles have the following elements: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>`, and `<Properties>`.</span></span> <span data-ttu-id="74dab-111">Das Standardprofil eines Geräts weist auch ein- `<Default>` Element auf.</span><span class="sxs-lookup"><span data-stu-id="74dab-111">The default profile of a device also has a `<Default>` element.</span></span>

<span data-ttu-id="74dab-112">Das `<ProfileGUID>` -Element und das- `<DeviceID>` Element können nicht geändert werden, nachdem das Scan Profil erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="74dab-112">The `<ProfileGUID>` element and the `<DeviceID>` element cannot be changed after the scan profile is created.</span></span> <span data-ttu-id="74dab-113">Die Werte des `<ProfileName>` -Elements und des- `<WiaItem>` Elements können geändert werden.</span><span class="sxs-lookup"><span data-stu-id="74dab-113">The values of the `<ProfileName>` element and the `<WiaItem>` element can be modified.</span></span> <span data-ttu-id="74dab-114">Das- `<Default>` Element kann hinzugefügt oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="74dab-114">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="74dab-115">Dies kann Programm gesteuert mithilfe der Methoden [**iscanprofile:: SetName**](-wia-iscanprofile-setname.md), [**iscanprofile:: SetItem**](-wia-iscanprofile-setitem.md)und [**iscanprofilemgr:: SetDefault**](-wia-iscanprofilemgr-setdefault.md) erfolgen.</span><span class="sxs-lookup"><span data-stu-id="74dab-115">This can be done programatically using the [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md), and [**IScanProfileMgr::SetDefault**](-wia-iscanprofilemgr-setdefault.md) methods.</span></span> <span data-ttu-id="74dab-116">Diese Eigenschaften können auch von Benutzern über die [**iscanprofileui:: scanprofiledialog**](-wia-iscanprofileui-scanprofiledialog.md) -Methode geändert werden.</span><span class="sxs-lookup"><span data-stu-id="74dab-116">These properties can also be changed by users through the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="74dab-117">Das- `<Properties>` Element enthält untergeordnete Elemente `<Property>` .</span><span class="sxs-lookup"><span data-stu-id="74dab-117">The `<Properties>` element contains `<Property>` children.</span></span> <span data-ttu-id="74dab-118">Verwenden Sie diese, um dem Profil eine beliebige WIA-Element-oder Geräte Eigenschaft hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="74dab-118">Use these to add any WIA item or device property to the profile.</span></span> <span data-ttu-id="74dab-119">Sie können auch Ihre eigenen Image-Erstell-untergeordneten Elemente entwickeln `<Property>` .</span><span class="sxs-lookup"><span data-stu-id="74dab-119">You can also develop your own image acquistion `<Property>` children.</span></span> <span data-ttu-id="74dab-120">Dadurch ist das Scan Profil Schema erweiterbar.</span><span class="sxs-lookup"><span data-stu-id="74dab-120">This makes the Scan Profile Schema extensible.</span></span> <span data-ttu-id="74dab-121">(Weitere Informationen zum Erweitern des Schemas finden Sie unter [Definieren von benutzerdefinierten Eigenschaften](-wia-defining-custom-properties.md), [**iscanprofile:: GetProperty**](-wia-iscanprofile-getproperty.md)und [**iscanprofile:: SetProperty**](-wia-iscanprofile-setproperty.md).)</span><span class="sxs-lookup"><span data-stu-id="74dab-121">(For more information about extending the schema, see [Defining Custom Properties](-wia-defining-custom-properties.md), [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md), and [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).)</span></span>

<span data-ttu-id="74dab-122">Hier ist das komplette Überprüfungs Profil Schema.</span><span class="sxs-lookup"><span data-stu-id="74dab-122">Here is the complete Scan Profile Schema.</span></span> <span data-ttu-id="74dab-123">Ein Beispiel Profil folgt.</span><span class="sxs-lookup"><span data-stu-id="74dab-123">A sample profile follows.</span></span>


```
<?xml version="1.0"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema"
            targetNamespace="https://www.microsoft.com"
            xmlns="https://www.microsoft.com"
            elementFormDefault="qualified">

<xs:element name="ScanProfile">
            <xs:complexType>
            <xs:sequence>
                        <xs:element name="ProfileGUID" type="xs:string"/>
                        <xs:element name="DeviceID" type="xs:string"/>
<xs:element name="ProfileName" type="xs:string"/>
                        <xs:element name="Default" minOccurs="0">
                                    <xs:complexType>
                                    </xs:complexType>
                        </xs:element>
                        <xs:element name="WiaItem" type="xs:string"/>
                        <xs:element name="Properties" type="Properties"/>
            </xs:sequence>
            </xs:complexType>
</xs:element>
 
<xs:complexType name="Properties">
<xs:sequence>
            <xs:element name="Property" maxOccurs="unbounded" minOccurs="0">
            <xs:complexType>
            <xs:simpleContent>
                        <xs:extension base="xs:string">
                                    <xs:attribute name="id" type="xs:integer" use="required"/>
                                    <xs:attribute name="type" type="xs:integer" use="required"/>
                        </xs:extension>
            </xs:simpleContent>
            </xs:complexType>
            </xs:element>
</xs:sequence>
</xs:complexType>
 
</xs:schema>
```



<span data-ttu-id="74dab-124">Klicken Sie auf **Beispiel anzeigen** , um ein Beispiel Profil anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="74dab-124">Click **Show Example** to see a sample profile.</span></span>


```
<ScanProfile>
    <ProfileGUID>
        {F862E217-32B0-4396-987A-2191224925CD}
    </ProfileGUID>
    <DeviceID>
        {6BDD1FC6-810F-11D0-BEC7-08002BE2092F}\0001
    </DeviceID>
    <ProfileName>
        Last used settings
    </ProfileName>
    <WiaItem>
        {FB607B1F-43F3-488B-855B-FB703EC342A6}
    </WiaItem>
    <Properties>
        <Property id="4103" type="3">
            3
        </Property>
        <Property id="4106" type="72">
            {B96B3CAB-0728-11D3-9D7B-0000F81EF32E}
        </Property>
        <Property id="6147" type="3">
            300
        </Property>
        <Property id="6154" type="3">
            0
        </Property>
        <Property id="6155" type="3">
            0
        </Property>
    </Properties>
</ScanProfile>
```



## <a name="related-topics"></a><span data-ttu-id="74dab-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="74dab-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="74dab-126">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="74dab-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="74dab-127">**Iscanprofile:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="74dab-127">**IScanProfile::GetProperty**</span></span>](-wia-iscanprofile-getproperty.md)
</dt> <dt>

[<span data-ttu-id="74dab-128">**Iscanprofile:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="74dab-128">**IScanProfile::SetProperty**</span></span>](-wia-iscanprofile-setproperty.md)
</dt> <dt>

<span data-ttu-id="74dab-129">**Licher**</span><span class="sxs-lookup"><span data-stu-id="74dab-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="74dab-130">WIA-Eigenschafts Konstanten</span><span class="sxs-lookup"><span data-stu-id="74dab-130">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="74dab-131">Definieren von benutzerdefinierten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74dab-131">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 



