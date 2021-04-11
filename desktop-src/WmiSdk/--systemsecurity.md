---
description: Enthält Methoden, mit denen Sie auf die Sicherheitseinstellungen für einen Namespace zugreifen und diese ändern können.
ms.assetid: a54fdd85-feb8-4727-9f26-fe4f213cab6b
ms.tgt_platform: multiple
title: __SystemSecurity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 58de990b56518550705cda2f8360cd90a0381c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132084"
---
# <a name="__systemsecurity-class"></a><span data-ttu-id="78eaf-103">\_\_SystemSecurity-Klasse</span><span class="sxs-lookup"><span data-stu-id="78eaf-103">\_\_SystemSecurity class</span></span>

<span data-ttu-id="78eaf-104">Die System **\_ \_ Security** -System Klasse enthält Methoden, mit denen Sie auf die Sicherheitseinstellungen für einen Namespace zugreifen und diese ändern können.</span><span class="sxs-lookup"><span data-stu-id="78eaf-104">The **\_\_SystemSecurity** system class contains methods that let you access and modify the security settings for a namespace.</span></span> <span data-ttu-id="78eaf-105">Die **\_ \_ SystemSecurity** -Klasse ist eine Singleton-Klasse in jedem Namespace.</span><span class="sxs-lookup"><span data-stu-id="78eaf-105">The **\_\_SystemSecurity** class is a singleton class in each namespace.</span></span>

> [!Note]  
> <span data-ttu-id="78eaf-106">Weitere Informationen finden Sie unter [Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="78eaf-106">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

 

<span data-ttu-id="78eaf-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="78eaf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="78eaf-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="78eaf-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="78eaf-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="78eaf-109">Syntax</span></span>

``` syntax
class __SystemSecurity
{
};
```

## <a name="members"></a><span data-ttu-id="78eaf-110">Member</span><span class="sxs-lookup"><span data-stu-id="78eaf-110">Members</span></span>

<span data-ttu-id="78eaf-111">Die **\_ \_ System Security** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="78eaf-111">The **\_\_SystemSecurity** class has these types of members:</span></span>

-   [<span data-ttu-id="78eaf-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="78eaf-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="78eaf-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="78eaf-113">Methods</span></span>

<span data-ttu-id="78eaf-114">Die **\_ \_ System Security** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="78eaf-114">The **\_\_SystemSecurity** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="78eaf-115">Methode</span><span class="sxs-lookup"><span data-stu-id="78eaf-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="78eaf-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78eaf-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="78eaf-117"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></span><span class="sxs-lookup"><span data-stu-id="78eaf-117"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="78eaf-118">Ruft eine Liste von Benutzern ab, denen der Remote Zugriff gestattet ist.</span><span class="sxs-lookup"><span data-stu-id="78eaf-118">Gets a list of users who are allowed remote access.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="78eaf-119">Diese Methode funktioniert nicht in unterstützten Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="78eaf-119">This method does not work on supported versions of Windows.</span></span> <span data-ttu-id="78eaf-120">Verwenden Sie stattdessen <a href="--systemsecurity-getsd.md"><strong>ge-d</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="78eaf-120">Use <a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="78eaf-121"><a href="--systemsecurity-getcalleraccessrights.md"><strong>Getcalleraccessrights</strong></a></span><span class="sxs-lookup"><span data-stu-id="78eaf-121"><a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="78eaf-122">Gibt eine Maske zurück, die jedem Bit entspricht, das einem Zugriffsrecht entspricht.</span><span class="sxs-lookup"><span data-stu-id="78eaf-122">Returns a mask with each bit that corresponds to an access right.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="78eaf-123"><a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a></span><span class="sxs-lookup"><span data-stu-id="78eaf-123"><a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="78eaf-124">Ruft den <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> für den Namespace ab, mit dem der Benutzer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="78eaf-124">Gets the <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> for the namespace to which the user is connected.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="78eaf-125"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="78eaf-125"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="78eaf-126">Ruft die Sicherheits Beschreibung ab, die den Zugriff auf den WMI-Namespace steuert, der der- <strong>__SystemSecurity</strong>Instanz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="78eaf-126">Gets the security descriptor that controls access to the WMI namespace associated with the instance of <strong>__SystemSecurity</strong>.</span></span> <span data-ttu-id="78eaf-127">Die Sicherheits Beschreibung wird als Instanz von<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="78eaf-127">The security descriptor is returned as an instance of<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="78eaf-128"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></span><span class="sxs-lookup"><span data-stu-id="78eaf-128"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="78eaf-129">Legt eine Liste von Benutzern fest, denen der Remote Zugriff gestattet ist.</span><span class="sxs-lookup"><span data-stu-id="78eaf-129">Sets a list of users who are allowed remote access.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="78eaf-130">Diese Methode funktioniert nicht in unterstützten Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="78eaf-130">This method does not work on supported versions of Windows.</span></span> <span data-ttu-id="78eaf-131">Verwenden <a href="--systemsecurity-setsd.md"><strong>Sie</strong></a> stattdessen "".</span><span class="sxs-lookup"><span data-stu-id="78eaf-131">Use <a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="78eaf-132"><a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a></span><span class="sxs-lookup"><span data-stu-id="78eaf-132"><a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="78eaf-133">Legt die Sicherheits Beschreibung für den Namespace fest, mit dem der Benutzer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="78eaf-133">Sets the security descriptor for the namespace to which the user is connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="78eaf-134"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SETSECURITYDESCRIPTOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="78eaf-134"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="78eaf-135">Schreibt eine aktualisierte Version der Sicherheits Beschreibung, die den Zugriff auf den Drucker steuert.</span><span class="sxs-lookup"><span data-stu-id="78eaf-135">Writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="78eaf-136">Die Sicherheits Beschreibung wird durch eine Instanz von <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>dargestellt.</span><span class="sxs-lookup"><span data-stu-id="78eaf-136">The security descriptor is represented by an instance of <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="78eaf-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78eaf-137">Remarks</span></span>

<span data-ttu-id="78eaf-138">Sie können festlegen, dass Client Skripts und-Anwendungen eine verschlüsselte Verbindung für die Authentifizierung verwenden, indem Sie der MOF-Datei, die den Namespace erstellt, den Wert "Requirements **sencryption** " hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="78eaf-138">You can require that client scripts and applications use an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the .mof file that creates the namespace.</span></span> <span data-ttu-id="78eaf-139">Sie können auch einen vorhandenen Namespace ändern, indem Sie dieses Attribut hinzufügen und die MOF-Datei erneut kompilieren.</span><span class="sxs-lookup"><span data-stu-id="78eaf-139">You can also modify an existing namespace by adding this attribute and compile the .mof file again.</span></span> <span data-ttu-id="78eaf-140">Weitere Informationen **zur Verwendung von**"Requirements" finden Sie unter [erfordern einer verschlüsselten Verbindung mit einem Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="78eaf-140">For more information about how to use **RequiresEncryption**, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78eaf-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78eaf-141">Requirements</span></span>



| <span data-ttu-id="78eaf-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78eaf-142">Requirement</span></span> | <span data-ttu-id="78eaf-143">Wert</span><span class="sxs-lookup"><span data-stu-id="78eaf-143">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="78eaf-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78eaf-144">Minimum supported client</span></span><br/> | <span data-ttu-id="78eaf-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78eaf-145">Windows Vista</span></span><br/>       |
| <span data-ttu-id="78eaf-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78eaf-146">Minimum supported server</span></span><br/> | <span data-ttu-id="78eaf-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78eaf-147">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="78eaf-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="78eaf-148">Namespace</span></span><br/>                | <span data-ttu-id="78eaf-149">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="78eaf-149">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="78eaf-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78eaf-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78eaf-151">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="78eaf-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="78eaf-152">WMI-Sicherheits Konstanten</span><span class="sxs-lookup"><span data-stu-id="78eaf-152">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="78eaf-153">WMI-sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="78eaf-153">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="78eaf-154">Sichern von WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="78eaf-154">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="78eaf-155">Einrichten der Vererbung der Namespace Sicherheit</span><span class="sxs-lookup"><span data-stu-id="78eaf-155">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="78eaf-156">Access Control Listen (ACLs)</span><span class="sxs-lookup"><span data-stu-id="78eaf-156">Access Control Lists (ACLs)</span></span>](/windows/desktop/SecAuthZ/access-control-lists)
</dt> <dt>

[<span data-ttu-id="78eaf-157">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78eaf-157">**Security\_Descriptor**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

