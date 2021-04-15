---
title: Wiederherstellen gelöschter Objekte
description: Windows Server 2003 enthält die Datei \ 0034; gelöschte Objekte wiederherstellen \ 0034; befinden.
ms.assetid: b64c5c91-fb76-4323-b78d-f692aa887c96
ms.tgt_platform: multiple
keywords:
- Wiederherstellen gelöschter Objekte AD
- Active Directory, verwenden, Wiederherstellen gelöschter Objekte
- Objekte AD, Wiederherstellen gelöschter Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f8f1d3511bb4246826e677aa239ca594918127a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104516703"
---
# <a name="restoring-deleted-objects"></a>Wiederherstellen gelöschter Objekte

Windows Server 2003 enthält das Feature "Gelöschte Objekte wiederherstellen".

Um die Wiederherstellung gelöschter Objekte zu aktivieren, muss mindestens ein Domänen Controller in der Domäne unter Windows Server 2003 oder einer höheren Version von Windows ausgeführt werden. Standardmäßig können nur Domänen Administratoren gelöschte Objekte wiederherstellen. Diese können jedoch an andere Personen delegiert werden.

Die folgenden Einschränkungen gelten für die Wiederherstellung von gelöschten Objekten:

-   Ein Objekt kann nicht wieder hergestellt werden, wenn die Tombstone-Lebensdauer für das Objekt abgelaufen ist, da das Objekt endgültig gelöscht wird, wenn die Tombstone-Lebensdauer abgelaufen ist.
-   Objekte, die im Stamm des Namens Kontexts vorhanden sind, z. b. eine Domänen-oder Anwendungs Partition, können nicht wieder hergestellt werden.
-   Schema Objekte können nicht wieder hergestellt werden. Schema Objekte sollten nie gelöscht werden.
-   Es ist möglich, gelöschte Container wiederherzustellen, aber die Wiederherstellung der gelöschten Objekte, die sich vor dem Löschen im Container befanden, ist schwierig, da die Baumstruktur unter dem Container manuell rekonstruiert werden muss.

## <a name="permissions-required-to-restore-a-deleted-object"></a>Erforderliche Berechtigungen zum Wiederherstellen eines gelöschten Objekts

Wenn ein Objekt gelöscht wird, wird die Objekt Sicherheits Beschreibung beibehalten. Obwohl der Besitzer von der Sicherheits Beschreibung identifiziert werden kann, können aus Sicherheitsgründen nur Domänen Administratoren gelöschte Objekte wiederherstellen. Domänen Administratoren können die Berechtigung zum Wiederherstellen von Lösch Objekten für andere Benutzer und Gruppen erteilen, indem Sie dem Benutzer oder der Gruppe das Kontroll Zugriffsrecht für das reanimieren von Tombstones erteilen. Das Kontroll Zugriffsrecht "reanimieren von Tombstones" wird im namens Kontext Stamm erteilt. Nur Benutzer mit Lese Zugriffsberechtigung für ein Objekt und seine Attribute dürfen das Objekt und barrierefreie Attribute lesen, nachdem das Objekt gelöscht wurde.

> [!Note]  
> Das Erteilen eines Benutzers diese Berechtigung kann ein Sicherheitsrisiko darstellen, da der Benutzer ein Konto Objekt wiederherstellen kann, das Zugriff auf Ressourcen hat, auf die der Benutzer normalerweise keinen Zugriff hat. Durch die Wiederherstellung eines Kontos erhält der Benutzer im Wesentlichen die Kontrolle über dieses Konto, da der Benutzer das anfängliche Kennwort für das Konto festlegen muss, wenn das Konto wieder hergestellt wird.

 

Zum vollständigen Wiederherstellen eines gelöschten Objekts muss der Benutzer folgende Aktionen ausführen:

-   Sie haben oder sind Mitglied einer Gruppe, die über das Steuerelement Zugriffsrecht zum reanimieren von Tombstones verfügt.

-   Sie haben Schreibzugriff auf jedes obligatorische Attribut, das aktualisiert werden muss.

-   Sie haben Schreibzugriff auf den relativen Distinguished Name (RDN).

-   Sie haben Schreibzugriff auf jedes optionale Attribut, das aktualisiert werden muss.

-   Übergeordnete Erstellungs Rechte für den Zielcontainer für die Objektklasse des wiederhergestellten Objekts verfügen.

    > [!Note]  
    > Das **isDeleted** -Attribut wird während des Wiederherstellungs Vorgangs nicht überprüft. Weder die Delete-Child-Berechtigung für den Container "Deleted Objects" wird überprüft.

     

## <a name="restoring-a-deleted-object"></a>Wiederherstellen eines gelöschten Objekts

Zum Wiederherstellen eines gelöschten Objekts muss sich das Objekt zuerst im Container Gelöschte Objekte befinden. Weitere Informationen zum Abrufen von gelöschten Objekten finden Sie unter [Abrufen gelöschter Objekte](retrieving-deleted-objects.md).

Wenn das Objekt gefunden wurde, müssen die folgenden Vorgänge in einem einzelnen LDAP-Vorgang abgeschlossen werden. Dies erfordert die Verwendung der LDAP-Funktion zum [**\_ Ändern von Ext- \_ \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) mit dem [**LDAP-Server " \_ \_ \_ gelöschtes \_ OID**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) -Steuerelement anzeigen"

-   Entfernen Sie den Wert des **isDeleted** -Attributs. Der Wert des **isDeleted** -Attributs muss entfernt und nicht auf " **false**" festgelegt werden.
-   Ersetzen Sie den Distinguished Name des Objekts, sodass er in einen anderen als den Container für gelöschte Objekte verschoben wird. Dies kann ein beliebiger Container sein, der normalerweise das-Objekt enthalten kann. Der Distinguished Name des vorherigen Containers des-Objekts befindet sich im **lastKnownParent** -Attribut des gelöschten Objekts. Das **lastKnownParent** -Attribut wird nur festgelegt, wenn das Objekt auf einem Windows Server 2003-Domänen Controller gelöscht wurde. Daher ist es möglich, dass der Inhalt des **lastKnownParent** -Attributs ungenau ist.
-   Stellen Sie die obligatorischen Attribute für das Objekt wieder her, die während des Löschvorgangs gelöscht wurden.

> [!Note]  
> Das **objectCategory** -Attribut kann auch festgelegt werden, wenn das Objekt wieder hergestellt wird, jedoch nicht erforderlich ist. Wenn kein **objectCategory** -Wert angegeben wird, wird die Standard- **objectCategory** für die **objectClass** des Objekts verwendet.

 

Nachdem das Objekt wieder hergestellt wurde, kann es wie vor dem Löschen aufgerufen werden. An diesem Punkt sollten alle optionalen Attribute, die wichtig sind, wieder hergestellt werden. Alle Verweise auf das Objekt aus anderen Objekten im Verzeichnis müssen ebenfalls wieder hergestellt werden.

Als Sicherheitsmaßnahme werden Benutzer Objekte deaktiviert, wenn Sie wieder hergestellt werden. Benutzer Objekte müssen aktiviert werden, nachdem die optionalen Attribute wieder hergestellt wurden, damit das Benutzerobjekt verwendet werden kann.

Weitere Informationen und ein Codebeispiel, das zeigt, wie ein gelöschtes Objekt wieder hergestellt wird, finden Sie unten in der Funktion restoredeletedobject.

## <a name="restoredeletedobject"></a>Restoredeletedobject

Im folgenden C++-Codebeispiel wird gezeigt, wie ein gelöschtes Objekt wieder hergestellt wird.


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



 

 