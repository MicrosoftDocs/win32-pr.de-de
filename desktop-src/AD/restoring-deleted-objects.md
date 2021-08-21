---
title: Wiederherstellen gelöschter Objekte
description: Windows Server 2003 enthält \ 0034;gelöschte Objekte wiederherstellen \ 0034; Feature.
ms.assetid: b64c5c91-fb76-4323-b78d-f692aa887c96
ms.tgt_platform: multiple
keywords:
- Wiederherstellen von Deleted Objects AD
- Active Directory mit, Wiederherstellen gelöschter Objekte
- Objekte AD , Wiederherstellen gelöschter Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 431bcddcbd15366a6accf9b8368fa8d34377b27af923fb102803b6316462634e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025118"
---
# <a name="restoring-deleted-objects"></a>Wiederherstellen gelöschter Objekte

Windows Server 2003 enthält das Feature "Gelöschte Objekte wiederherstellen".

Um die Wiederherstellung gelöschter Objekte zu aktivieren, muss mindestens ein Domänencontroller in der Domäne auf Windows Server 2003 oder einer neueren Version von Windows. Standardmäßig können nur Domänenadministratoren gelöschte Objekte wiederherstellen, obwohl dies an andere Benutzer delegiert werden kann.

Die folgenden Einschränkungen gelten für die Wiederherstellung gelöschter Objekte:

-   Ein Objekt kann nicht wiederhergestellt werden, wenn die Tombstonelebensdauer für das Objekt abgelaufen ist, da das Objekt nach Ablauf der Tombstonelebensdauer dauerhaft gelöscht wird.
-   Objekte, die sich im Stamm des Namenskontexts befinden, z. B. eine Domäne oder Anwendungspartition, können nicht wiederhergestellt werden.
-   Schemaobjekte können nicht wiederhergestellt werden. Schemaobjekte sollten nie gelöscht werden.
-   Gelöschte Container können wiederhergestellt werden, aber die Wiederherstellung der gelöschten Objekte, die vor dem Löschen im Container waren, ist schwierig, da die Struktur unter dem Container manuell rekonstruiert werden muss.

## <a name="permissions-required-to-restore-a-deleted-object"></a>Erforderliche Berechtigungen zum Wiederherstellen eines gelöschten Objekts

Wenn ein Objekt gelöscht wird, wird der Objektsicherheitsdeskriptor beibehalten. Obwohl der Besitzer anhand des Sicherheitsdeskriptors identifizierbar ist, dürfen aus Sicherheitsgründen nur Domänenadministratoren gelöschte Objekte wiederherstellen. Domänenadministratoren können anderen Benutzern und Gruppen die Berechtigung zum Wiederherstellen von Löschobjekten erteilen, indem sie dem Benutzer oder der Gruppe das Steuerelementzugriffsrecht "Tombstone reanimate" gewähren. Das Zugriffsrecht "Reanimate Tombstone" wird im Stammverzeichnis des Namenskontexts gewährt. Nur Benutzer mit Lesezugriffsberechtigung für ein Objekt und dessen Attribute dürfen das Objekt und die zugänglichen Attribute lesen, nachdem das Objekt gelöscht wurde.

> [!Note]  
> Das Erteilen dieser Berechtigung für einen Benutzer kann ein Sicherheitsrisiko darstellen, da es dem Benutzer ermöglichen könnte, ein Kontoobjekt wiederherzustellen, das Zugriff auf Ressourcen hat, auf die der Benutzer normalerweise keinen Zugriff hätte. Durch das Wiederherstellen eines Kontos erhält der Benutzer im Wesentlichen die Kontrolle über dieses Konto, da der Benutzer das anfängliche Kennwort für das Konto festlegen muss, wenn das Konto wiederhergestellt wird.

 

Um ein gelöschtes Objekt vollständig wiederherzustellen, muss der Benutzer:

-   Sie müssen mitglied einer Gruppe sein, die über das Zugriffsrecht "Tombstone reanimate" verfügt.

-   Verfügen Sie über Schreibzugriff für jedes obligatorische Attribut, das aktualisiert werden muss.

-   Schreibzugriff auf den relativen Distinguished Name (RDN).

-   Schreibzugriff auf jedes optionale Attribut, das aktualisiert werden muss.

-   Sie verfügen über untergeordnete Erstellungsrechte für den Zielcontainer für die Objektklasse des wiederhergestellten Objekts.

    > [!Note]  
    > Das **attribut isDeleted** wird während des Wiederherstellungsvorgang nicht überprüft. Die Berechtigung delete-child für den Container "Deleted Objects" wird nicht überprüft.

     

## <a name="restoring-a-deleted-object"></a>Wiederherstellen eines gelöschten Objekts

Um ein gelöschtes Objekt wiederherzustellen, muss sich das Objekt zuerst im Container Gelöschte Objekte befinden. Weitere Informationen zum Abrufen gelöschter Objekte finden Sie unter [Retrieving Deleted Objects](retrieving-deleted-objects.md).

Wenn das Objekt gefunden wurde, müssen die folgenden Vorgänge in einem einzelnen LDAP-Vorgang abgeschlossen werden. Dies erfordert die Verwendung der [**funktion ldap modify ext \_ \_ \_ mit**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) dem [**LDAP SERVER SHOW \_ \_ \_ \_ DELETED OID-Steuerelement.**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid)

-   Entfernen Sie den **IsDeleted-Attributwert.** Der **IsDeleted-Attributwert** muss entfernt und nicht auf **FALSE festgelegt werden.**
-   Ersetzen Sie den Distinguished Name des Objekts, sodass es in einen anderen Container als den Container gelöschte Objekte verschoben wird. Dies kann ein beliebiger Container sein, der normalerweise das -Objekt enthalten kann. Der Distinguished Name des vorherigen Containers des Objekts finden Sie im **lastKnownParent-Attribut** des gelöschten Objekts. Das **lastKnownParent-Attribut** wird nur festgelegt, wenn das Objekt auf einem serverseitigen Server 2003-Domänencontroller Windows wurde. Daher ist es möglich, dass der Inhalt des **lastKnownParent-Attributs** ungenau ist.
-   Stellen Sie die obligatorischen Attribute für das Objekt wieder sicher, die während des Löschens gelöscht wurden.

> [!Note]  
> Das **objectCategory-Attribut** kann auch festgelegt werden, wenn das Objekt wiederhergestellt wird, aber nicht erforderlich ist. Wenn **kein objectCategory-Wert** angegeben wird, wird die **Standardobjektkategorie** für **objectClass des** Objekts verwendet.

 

Nachdem das Objekt wiederhergestellt wurde, kann auf es wie vor dem Löschen zugegriffen werden. An diesem Punkt sollten alle optionalen Attribute, die wichtig sind, wiederhergestellt werden. Alle Verweise auf das Objekt aus anderen Objekten im Verzeichnis müssen ebenfalls wiederhergestellt werden.

Als Sicherheitsmaßnahme werden Benutzerobjekte deaktiviert, wenn sie wiederhergestellt werden. Benutzerobjekte müssen nach dem Wiederherstellen der optionalen Attribute aktiviert werden, damit das Benutzerobjekt verwendet werden kann.

Weitere Informationen und ein Codebeispiel, das zeigt, wie ein gelöschtes Objekt wiederhergestellt wird, finden Sie weiter unten in der RestoreDeletedObject-Funktion.

## <a name="restoredeletedobject"></a>RestoreDeletedObject

Das folgende C++-Codebeispiel zeigt, wie ein gelöschtes Objekt wiederhergestellt wird.


```C++
//***************************************************************************
//
//  RestoreDeletedObject()
//
//  Restores a deleted object. 
//
//  pwszDeletedDN - Contains the fully qualified distinguished name of the 
//  deleted object.
//
//  pwszDestContainerDN - Contains the fully qualified distinguished name of 
//  the folder that the deleted object should be moved to.
//
//  Returns S_OK if successful or an HRESULT or LDAP error code otherwise.
//
//***************************************************************************

HRESULT RestoreDeletedObject(LPCWSTR pwszDeletedDN, LPCWSTR pwszDestContainerDN)
{
    if((NULL == pwszDeletedDN) || (NULL == pwszDestContainerDN))
    {
        return E_POINTER;
    }
    
    HRESULT hr = E_FAIL;

    // Build the new distinguished name.
    LPWSTR pwszNewDN = new WCHAR[lstrlenW(pwszDeletedDN) + lstrlenW(pwszDestContainerDN) + 1];
    if(pwszNewDN)
    {
        wcscpy_s(pwszNewDN, pwszDeletedDN);

        // Search for the first 0x0A character. This is the delimiter in the deleted object name.
        LPWSTR pwszChar;
        for(pwszChar = pwszNewDN; *pwszChar; pwszChar = CharNextW(pwszChar))
        {
            if(('\\' == *pwszChar) && ('0' == *(pwszChar + 1)) && ('A' == *(pwszChar + 2)))
            {
                break;
            }
            
        }

        if(0 != *pwszChar)
        {
            // Truncate the name string at the delimiter.
            *pwszChar = 0;

            // Add the last known parent DN to complete the DN.
            wcscat_s(pwszNewDN, L",");
            wcscat_s(pwszNewDN, pwszDestContainerDN);

            PLDAP ld;

            // Initialize LDAP.
            ld = ldap_init(NULL, LDAP_PORT);
            if(NULL != ld) 
            {
                ULONG ulRC;
                ULONG version = LDAP_VERSION3;

                // Set the LDAP version.
                ulRC = ldap_set_option(ld, LDAP_OPT_PROTOCOL_VERSION, (void*)&version);
                if(LDAP_SUCCESS == ulRC)
                {
                    // Establish a connection with the server.
                    ulRC = ldap_connect(ld, NULL);
                    if(LDAP_SUCCESS == ulRC)
                    {                    
                        // Bind to the LDAP server.
                        ulRC = ldap_bind_s(ld, NULL, NULL, LDAP_AUTH_NEGOTIATE);
                        if(LDAP_SUCCESS == ulRC)
                        {
                            // Setup the new values.
                            LPWSTR rgNewVals[] = {pwszNewDN, NULL};

                            /*
                            Remove the isDeleted attribute. This cannot be set 
                            to FALSE or the restore operation will not work.
                            */
                            LDAPModW modIsDeleted = { LDAP_MOD_DELETE, L"isDeleted", NULL };

                            /*
                            Set the new DN, in effect, moving the deleted 
                            object to where it resided before the deletion.
                            */
                            LDAPModW modDN = { LDAP_MOD_REPLACE, L"distinguishedName", rgNewVals };
                            
                            // Initialize the LDAPMod structure.
                            PLDAPModW ldapMods[] = 
                            {
                                &modIsDeleted,
                                &modDN,
                                NULL
                            };

                            /*
                            Use the LDAP_SERVER_SHOW_DELETED_OID control to 
                            modify deleted objects.
                            */
                            LDAPControlW showDeletedControl;
                            showDeletedControl.ldctl_oid = LDAP_SERVER_SHOW_DELETED_OID_W;
                            showDeletedControl.ldctl_value.bv_len = 0;
                            showDeletedControl.ldctl_value.bv_val = NULL;
                            showDeletedControl.ldctl_iscritical = TRUE;

                            // Initialzie the LDAPControl structure
                            PLDAPControlW ldapControls[] = { &showDeletedControl, NULL };

                            /*
                            Modify the specified attributes. This must performed 
                            in one step, which is why the LDAP APIs must be used 
                            to restore a deleted object.
                            */
                            ulRC = ldap_modify_ext_sW(ld, (PWCHAR)pwszDeletedDN, ldapMods, ldapControls, NULL);
                            if(LDAP_SUCCESS == ulRC)
                            {
                                hr = S_OK;
                            }
                            else if(LDAP_ALREADY_EXISTS == ulRC)
                            {
                                /*
                                An object already exists with the specified name 
                                in the specified target container. At this point, 
                                a new name must be selected.
                                */
                            }
                        }
                    }
                }

                if(LDAP_SUCCESS != ulRC)
                {
                    hr = ulRC;
                    
                    OutputDebugString(ldap_err2string(ulRC));
                }

                // Release the LDAP session.
                ldap_unbind(ld);
            }
        }
        else
        {
            /*
            If the end of the string is reached before the delimiter is found, just 
            end and fail.
            */
            hr = E_INVALIDARG;
        }
    
        delete pwszNewDN;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }

    return hr;
}

```



 

 